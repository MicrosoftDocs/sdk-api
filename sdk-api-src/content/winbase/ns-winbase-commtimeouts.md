---
UID: NS:winbase._COMMTIMEOUTS
title: COMMTIMEOUTS (winbase.h)
description: Contains the time-out parameters for a communications device.
helpviewer_keywords: ["*LPCOMMTIMEOUTS","COMMTIMEOUTS","COMMTIMEOUTS structure","LPCOMMTIMEOUTS","LPCOMMTIMEOUTS structure pointer","_COMMTIMEOUTS","_win32_commtimeouts_str","base.commtimeouts_str","winbase/COMMTIMEOUTS","winbase/LPCOMMTIMEOUTS"]
old-location: base\commtimeouts_str.htm
tech.root: base
ms.assetid: 259aa110-b2c3-4583-a3f9-805a42025a81
ms.date: 12/05/2018
ms.keywords: '*LPCOMMTIMEOUTS, COMMTIMEOUTS, COMMTIMEOUTS structure, LPCOMMTIMEOUTS, LPCOMMTIMEOUTS structure pointer, _COMMTIMEOUTS, _win32_commtimeouts_str, base.commtimeouts_str, winbase/COMMTIMEOUTS, winbase/LPCOMMTIMEOUTS'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: COMMTIMEOUTS, *LPCOMMTIMEOUTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COMMTIMEOUTS
 - winbase/_COMMTIMEOUTS
 - LPCOMMTIMEOUTS
 - winbase/LPCOMMTIMEOUTS
 - COMMTIMEOUTS
 - winbase/COMMTIMEOUTS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbase.h
api_name:
 - COMMTIMEOUTS
---

# COMMTIMEOUTS structure


## -description

Contains the time-out parameters for a communications device. The parameters determine the 
    behavior of <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>, 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>, 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a>, and 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a> operations on the device.

## -struct-fields

### -field ReadIntervalTimeout

The maximum time allowed to elapse before the arrival of the next byte on the communications line, in 
       milliseconds. If the interval between the arrival of any two bytes exceeds this amount, the 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> operation is completed and any buffered data is 
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
    <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> function is called:

<ul>
<li>If there are any bytes in the input buffer, 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> returns immediately with the bytes in the 
      buffer.</li>
<li>If there are no bytes in the input buffer, <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> 
      waits until a byte arrives and then returns immediately.</li>
<li>If no bytes arrive within the time specified by <b>ReadTotalTimeoutConstant</b>, 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> times out.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getcommtimeouts">GetCommTimeouts</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setcommtimeouts">SetCommTimeouts</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a>