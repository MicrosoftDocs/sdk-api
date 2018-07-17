---
UID: NS:winbase._COMMTIMEOUTS
title: "_COMMTIMEOUTS"
author: windows-sdk-content
description: Contains the time-out parameters for a communications device.
old-location: base\commtimeouts_str.htm
old-project: DevIO
ms.assetid: 259aa110-b2c3-4583-a3f9-805a42025a81
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: "*LPCOMMTIMEOUTS, COMMTIMEOUTS, COMMTIMEOUTS structure, LPCOMMTIMEOUTS, LPCOMMTIMEOUTS structure pointer, _COMMTIMEOUTS, _win32_commtimeouts_str, base.commtimeouts_str, winbase/COMMTIMEOUTS, winbase/LPCOMMTIMEOUTS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: COMMTIMEOUTS, *LPCOMMTIMEOUTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbase.h
api_name:
 - COMMTIMEOUTS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _COMMTIMEOUTS structure


## -description


Contains the time-out parameters for a communications device. The parameters determine the 
    behavior of <a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a>, 
    <a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>, 
    <a href="https://msdn.microsoft.com/6c1a4de1-6cae-4c35-bfba-0bc252fadbd9">ReadFileEx</a>, and 
    <a href="https://msdn.microsoft.com/6995c4ee-ba91-41d5-b72d-19dc2eb95945">WriteFileEx</a> operations on the device.


## -struct-fields




### -field ReadIntervalTimeout

The maximum time allowed to elapse before the arrival of the next byte on the communications line, in 
       milliseconds. If the interval between the arrival of any two bytes exceeds this amount, the 
       <a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a> operation is completed and any buffered data is 
       returned. A value of zero indicates that interval time-outs are not used.

A value of <b>MAXDWORD</b>, combined with zero values for both the 
       <b>ReadTotalTimeoutConstant</b> and <b>ReadTotalTimeoutMultiplier</b> 
       members, specifies that the read operation is to return immediately with the bytes that have already been 
       received, even if no bytes have been received.


### -field ReadTotalTimeoutMultiplier

The multiplier used to calculate the total time-out period for read operations, in milliseconds. For each 
      read operation, this value is multiplied by the requested number of bytes to be read.


### -field ReadTotalTimeoutConstant

A constant used to calculate the total time-out period for read operations, in milliseconds. For each read 
       operation, this value is added to the product of the <b>ReadTotalTimeoutMultiplier</b> 
       member and the requested number of bytes.

A value of zero for both the <b>ReadTotalTimeoutMultiplier</b> and 
       <b>ReadTotalTimeoutConstant</b> members indicates that total time-outs are not used for 
       read operations.


### -field WriteTotalTimeoutMultiplier

The multiplier used to calculate the total time-out period for write operations, in milliseconds. For each 
      write operation, this value is multiplied by the number of bytes to be written.


### -field WriteTotalTimeoutConstant

A constant used to calculate the total time-out period for write operations, in milliseconds. For each write 
       operation, this value is added to the product of the <b>WriteTotalTimeoutMultiplier</b> 
       member and the number of bytes to be written.

A value of zero for both the <b>WriteTotalTimeoutMultiplier</b> and 
       <b>WriteTotalTimeoutConstant</b> members indicates that total time-outs are not used for 
       write operations.


## -remarks



If an application sets <b>ReadIntervalTimeout</b> and 
    <b>ReadTotalTimeoutMultiplier</b> to <b>MAXDWORD</b> and sets 
    <b>ReadTotalTimeoutConstant</b> to a value greater than zero and less than 
    <b>MAXDWORD</b>, one of the following occurs when the 
    <a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a> function is called:

<ul>
<li>If there are any bytes in the input buffer, 
      <a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a> returns immediately with the bytes in the 
      buffer.</li>
<li>If there are no bytes in the input buffer, <a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a> 
      waits until a byte arrives and then returns immediately.</li>
<li>If no bytes arrive within the time specified by <b>ReadTotalTimeoutConstant</b>, 
      <a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a> times out.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/a5375b2e-0992-4e47-a20f-8a793addeef6">GetCommTimeouts</a>



<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a>



<a href="https://msdn.microsoft.com/6c1a4de1-6cae-4c35-bfba-0bc252fadbd9">ReadFileEx</a>



<a href="https://msdn.microsoft.com/71aa6ab3-d56c-43bc-9932-5b4e61fc4b30">SetCommTimeouts</a>



<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>



<a href="https://msdn.microsoft.com/6995c4ee-ba91-41d5-b72d-19dc2eb95945">WriteFileEx</a>
 

 

