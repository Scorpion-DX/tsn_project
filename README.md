## **To rebuild TSN project:**

    source tsn_ip_warpper.tcl
 
Vivado TSN project will be built in <work_space>/zcu_TSN
  ## To use the cracked TSN IP
  
in vivado project manager ,click "Settings".![vivado project manager](README_md_files/image.png?v=1&type=image
 select IP tab , and add "./ip" to ip dictionary
![IP settings](README_md_files/1.png?v=1&type=image)

## To repackage the cracked TSN IP

 1. create a new vivado RTL project
 2. add all file in "./ip/src" into project.
 3. set tsn_endpoint_ethernet_mac_0 as top in Hierarchy
 ![输入图片描述](README_md_files/2.png?v=1&type=image)
 4. in library window , change 6 files' library in "Design Sorces > VHDL" from "xilinx_defaultlib" to  "file_location".
 Such as file fifo_generator_v13_1_rfs.vhd , its location is ./ip/src/fifo_generator_v13_1_4 , change its library to "fifo_generator_v13_1_4"
 ![输入图片描述](README_md_files/3.png?v=1&type=image)
after modified , Libraries should be like this
![输入图片描述](README_md_files/4.png?v=1&type=image)
then run systhesis , after successfully systhesis , using "Tools > Create and package new ip" to package the cracked TSN IP.
