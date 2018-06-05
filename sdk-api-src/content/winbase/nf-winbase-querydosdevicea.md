---
UID: NF:winbase.QueryDosDeviceA
title: QueryDosDeviceA function
author: windows-sdk-content
description: Retrieves information about MS-DOS device names.
old-location: fs\querydosdevice.htm
old-project: FileIO
ms.assetid: ff25bc2b-dde6-40c3-a270-372daab2e5c4
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: QueryDosDevice, QueryDosDevice function [Files], QueryDosDeviceA, QueryDosDeviceW, _win32_querydosdevice, base.querydosdevice, fileapi/QueryDosDevice, fileapi/QueryDosDeviceA, fileapi/QueryDosDeviceW, fs.querydosdevice, winbase/QueryDosDevice, winbase/QueryDosDeviceA, winbase/QueryDosDeviceW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-File-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-File-l1-2-0.dll
-	API-MS-Win-Core-File-l1-2-1.dll
-	API-MS-Win-Core-File-l1-2-2.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
-	API-Ms-Win-Core-File-Ansi-L1-1-0.dll
-	Kernel32Legacy.dll
api_name:
-	QueryDosDevice
-	QueryDosDeviceA
-	QueryDosDeviceW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# QueryDosDeviceA function


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
       backslash; for example, use "C:", not "C:\".

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
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the buffer is too small, the function fails and the last error code is 
       <b>ERROR_INSUFFICIENT_BUFFER</b>.




## -remarks



The <a href="https://msdn.microsoft.com/924b1456-b2c5-4d52-aacf-6172608c73ea">DefineDosDevice</a> function enables an application 
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
     <a href="https://msdn.microsoft.com/7d802e9f-dc09-4e3d-b064-e9b57af396e2">Defining an MS DOS Device Name</a>.

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
     <a href="https://msdn.microsoft.com/359673bf-cc4c-4881-b946-ecdbef4a7ecb">Obtaining a File Name From a File Handle</a> 
     or <a href="https://msdn.microsoft.com/a9ee8cc8-fa62-4fc9-aa69-35ee98afe417">Displaying Volume Paths</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/924b1456-b2c5-4d52-aacf-6172608c73ea">DefineDosDevice</a>



<a href="https://msdn.microsoft.com/dc985126-970c-49f2-877f-3759125e43b6">Volume Management Functions</a>
 

 

