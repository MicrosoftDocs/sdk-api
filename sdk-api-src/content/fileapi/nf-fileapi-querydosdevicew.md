---
UID: NF:fileapi.QueryDosDeviceW
title: QueryDosDeviceW function (fileapi.h)
description: Retrieves information about MS-DOS device names. (QueryDosDeviceW)
helpviewer_keywords: ["QueryDosDevice","QueryDosDevice function [Files]","QueryDosDeviceA","QueryDosDeviceW","_win32_querydosdevice","base.querydosdevice","fileapi/QueryDosDevice","fileapi/QueryDosDeviceA","fileapi/QueryDosDeviceW","fs.querydosdevice","winbase/QueryDosDevice","winbase/QueryDosDeviceA","winbase/QueryDosDeviceW"]
old-location: fs\querydosdevice.htm
tech.root: fs
ms.assetid: ff25bc2b-dde6-40c3-a270-372daab2e5c4
ms.date: 12/05/2018
ms.keywords: QueryDosDevice, QueryDosDevice function [Files], QueryDosDeviceA, QueryDosDeviceW, _win32_querydosdevice, base.querydosdevice, fileapi/QueryDosDevice, fileapi/QueryDosDeviceA, fileapi/QueryDosDeviceW, fs.querydosdevice, winbase/QueryDosDevice, winbase/QueryDosDeviceA, winbase/QueryDosDeviceW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QueryDosDeviceW (Unicode) and QueryDosDeviceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryDosDeviceW
 - fileapi/QueryDosDeviceW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-Ms-Win-Core-File-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - QueryDosDevice
 - QueryDosDeviceA
 - QueryDosDeviceW
---

# QueryDosDeviceW function


## -description

Retrieves information about MS-DOS device names. The function can obtain the current 
    mapping for a particular MS-DOS device name. The function can also obtain a list of all existing MS-DOS device 
    names.

MS-DOS device names are stored as junctions in the object namespace. The code that converts an MS-DOS path into 
    a corresponding path uses these junctions to map MS-DOS devices and drive letters. The 
    <b>QueryDosDevice</b> function enables an application to query 
    the names of the junctions used to implement the MS-DOS device namespace as well as the value of each specific 
    junction.

## -parameters

### -param lpDeviceName [in, optional]

An MS-DOS device name string specifying the target of the query. The device name cannot have a trailing 
       backslash; for example, use "C:", not "C:\\".

This parameter can be <b>NULL</b>. In that case, the 
       <b>QueryDosDevice</b> function will store a list of all 
       existing MS-DOS device names into the buffer pointed to by <i>lpTargetPath</i>.

### -param lpTargetPath [out]

A pointer to a buffer that will receive the result of the query. The function fills this buffer with one or 
       more null-terminated strings. The final null-terminated string is followed by an additional 
       <b>NULL</b>.

If <i>lpDeviceName</i> is non-<b>NULL</b>, the function retrieves 
       information about the particular MS-DOS device specified by <i>lpDeviceName</i>. The first 
       null-terminated string stored into the buffer is the current mapping for the device. The other null-terminated 
       strings represent undeleted prior mappings for the device.

If <i>lpDeviceName</i> is <b>NULL</b>, the function retrieves a list of 
       all existing MS-DOS device names. Each null-terminated string stored into the buffer is the name of an existing 
       MS-DOS device, for example, \Device\HarddiskVolume1 or \Device\Floppy0.

### -param ucchMax [in]

The maximum number of <b>TCHARs</b> that can be stored into the buffer pointed to by 
      <i>lpTargetPath</i>.

## -returns

If the function succeeds, the return value is the number of <b>TCHARs</b> stored into 
       the buffer pointed to by <i>lpTargetPath</i>.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the buffer is too small, the function fails and the last error code is 
       <b>ERROR_INSUFFICIENT_BUFFER</b>.

## -remarks

The <a href="/windows/desktop/api/fileapi/nf-fileapi-definedosdevicew">DefineDosDevice</a> function enables an application 
    to create and modify the junctions used to implement the MS-DOS device namespace.

<b>Windows Server 2003 and Windows XP:  </b><b>QueryDosDevice</b> first searches the Local MS-DOS 
     Device namespace for the specified device name. If the device name is not found, the function will then search 
     the Global MS-DOS Device namespace.

When all existing MS-DOS device names are queried, the list of device names that are returned is dependent on 
     whether it is running in the "LocalSystem" context. If so, only the device names included in the Global MS-DOS 
     Device namespace will be returned. If not, a concatenation of the device names in the Global and Local MS-DOS 
     Device namespaces will be returned. If a device name exists in both namespaces, 
     <b>QueryDosDevice</b> will return the entry in the Local MS-DOS 
     Device namespace.

For more information on the Global and Local MS-DOS Device namespaces and changes to the accessibility of 
     MS-DOS device names, see 
     <a href="/windows/desktop/FileIO/defining-an-ms-dos-device-name">Defining an MS DOS Device Name</a>.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>
 

SMB does not support volume management functions.


#### Examples

For an example, see 
     <a href="/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle">Obtaining a File Name From a File Handle</a> 
     or <a href="/windows/desktop/FileIO/displaying-volume-paths">Displaying Volume Paths</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-definedosdevicew">DefineDosDevice</a>



<a href="/windows/desktop/FileIO/volume-management-functions">Volume Management Functions</a>
