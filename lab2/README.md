# Lab #2

## Overview

- Release Date: Monday, March 22
- **Due Date: @ 11:59pm**
- If you have any questions, please contact me via email (Mijin An / meeeeejin@gmail.com)

> NOTE: This lab is based on the Linux environment. If you don't have a Linux machine, use [VirturalBox](https://www.virtualbox.org/). (Recommend Ubuntu 18.04)

## Instructions

### Mount devices (Optional)

- If you have more than one storage device on your PC, read and try [this guide](reference/mount-guide.md) to separate data and log devices

### Install MySQL 5.7 and TPC-C

- Follow the [installation guide](reference/tpcc-mysql-install-guide.md) to install and run TPC-C benchmark on MySQL 5.7

### Collect performance metrics 

- Refer to the [performance analysis guide](reference/performance-analysis-guide.md) to gather performance metrics while running the TPC-C benchmark on MySQL 5.7
- **Follow the instructions below to fill out and submit a report**
    1. Check your system's spec by referring to the [guide](reference/performance-analysis-guide.md) and specify it in the report. For example:

    |:-----------:|:----------------------------------------------------------:|
    | OS          | Ubuntu 18.04.5 LTS                                         |
    | CPU         | Intel(R) Xeon(R) Silver 4216 CPU @ 2.10GHz (Total 32 cores)|
    | Memory      | 32GB                                                       |
    | Kernel      | 5.4.0-66-generic                                           |
    | Data Device | Intel® Optane™ SSD 900P Series 480GB                       |
    | Log Device  | Samsung 850 PRO SSD 256GB                                  |

    2. Specify the experimental environment of MySQL and TPC-C. For example:

    |:----------------:|:----------------------:|
    | DB size          | 2GB (20 warehouse)     |
    | Buffer Pool Size | 500MB, 1GB (25% and 50% of DB size, respectively) |
    | Benchmark Tool   | tpcc-mysql             |
    | Measure Time     | 1200s                  |
    | Connections      | 8                      |

    3. Run the TPC-C benchmark by varying the buffer pool size (`innodb_buffer_pool_size`) in the `my.cnf` file (e.g., 25% and 50% of DB size, respectively)

    4. *While running the benchmark*, collect performance metrics (I/O status and hit ratio) and record them in a separate file for future analysis
    
    5. After the benchmark ends, take a screenshot of the TPC-C output and add it to your report

    6. Combine all the results and analyze how the change in buffer pool size affected MySQL and the overall system's performance. Also, compare how I/O performance metrics change and draw your own conclusions

## Submission

Submit **a single PDF file** named `LAB2_STUDENTID_NAME.pdf` (e.g., `LAB2_2021123456_MijinAn`) to **i-Campus**.

- There is no page limit for the report