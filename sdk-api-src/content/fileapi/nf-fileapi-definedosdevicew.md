---
UID: NF:fileapi.DefineDosDeviceW
title: DefineDosDeviceW function
author: windows-sdk-content
description: Defines, redefines, or deletes MS-DOS device names.
old-location: fs\definedosdevice.htm
old-project: FileIO
ms.assetid: 924b1456-b2c5-4d52-aacf-6172608c73ea
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: DDD_EXACT_MATCH_ON_REMOVE, DDD_NO_BROADCAST_SYSTEM, DDD_RAW_TARGET_PATH, DDD_REMOVE_DEFINITION, DefineDosDevice, DefineDosDevice function [Files], DefineDosDeviceA, DefineDosDeviceW, _win32_definedosdevice, base.definedosdevice, fileapi/DefineDosDevice, fileapi/DefineDosDeviceA, fileapi/DefineDosDeviceW, fs.definedosdevice, winbase/DefineDosDevice, winbase/DefineDosDeviceA, winbase/DefineDosDeviceW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DefineDosDeviceW (Unicode) and DefineDosDeviceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STREAM_INFO_LEVELS
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
-	DefineDosDevice
-	DefineDosDeviceA
-	DefineDosDeviceW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# DefineDosDeviceW function


## -description


Defines, redefines, or deletes MS-DOS device names.


## -parameters




### -param dwFlags [in]

The controllable aspects of the <b>DefineDosDevice</b> function. This parameter 
      can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DDD_EXACT_MATCH_ON_REMOVE"></a><a id="ddd_exact_match_on_remove"></a><dl>
<dt><b>DDD_EXACT_MATCH_ON_REMOVE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
If this value is specified along with <b>DDD_REMOVE_DEFINITION</b>, the function will 
        use an exact match to determine which mapping to remove. Use this value to ensure that you do not delete 
        something that you did not define.

</td>
</tr>
<tr>
<td width="40%"><a id="DDD_NO_BROADCAST_SYSTEM"></a><a id="ddd_no_broadcast_system"></a><dl>
<dt><b>DDD_NO_BROADCAST_SYSTEM</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Do not broadcast the <a href="https://msdn.microsoft.com/77174e06-a25b-440a-9e9c-4fd5979c433c">WM_SETTINGCHANGE</a> message. 
        By default, this message is broadcast to notify the shell and applications of the change.

</td>
</tr>
<tr>
<td width="40%"><a id="DDD_RAW_TARGET_PATH"></a><a id="ddd_raw_target_path"></a><dl>
<dt><b>DDD_RAW_TARGET_PATH</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Uses the <i>lpTargetPath</i> string as is. Otherwise, it is converted from an MS-DOS 
        path to a path.

</td>
</tr>
<tr>
<td width="40%"><a id="DDD_REMOVE_DEFINITION"></a><a id="ddd_remove_definition"></a><dl>
<dt><b>DDD_REMOVE_DEFINITION</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Removes the specified definition for the specified device. To determine which definition to remove, the 
         function walks the list of mappings for the device, looking for a match of 
         <i>lpTargetPath</i> against a prefix of each mapping associated with this device. The 
         first mapping that matches is the one removed, and then the function returns.

If <i>lpTargetPath</i> is <b>NULL</b> or a pointer to a 
         <b>NULL</b> string, the function will remove the first mapping associated with the device 
         and pop the most recent one pushed. If there is nothing left to pop, the device name will be removed.

If this value is not specified, the string pointed to by the <i>lpTargetPath</i> 
         parameter will become the new mapping for this device.

</td>
</tr>
</table>
 


### -param lpDeviceName [in]

A pointer to an MS-DOS device name string specifying the device the function is defining, redefining, or 
      deleting. The device name string must not have a colon as the last character, unless a drive letter is being 
      defined, redefined, or deleted. For example, drive C  would be the string "C:". In no case is a 
      trailing backslash ("\") allowed.


### -param lpTargetPath [in, optional]

A pointer to a path string that will implement this device. The string is an MS-DOS path string unless the 
      <b>DDD_RAW_TARGET_PATH</b> flag is specified, in which case this string is a path 
      string.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



MS-DOS device names are stored as junctions in the object namespace. The code that converts an MS-DOS path 
    into a corresponding path uses these junctions to map MS-DOS devices and drive letters. The 
    <b>DefineDosDevice</b> function enables an application to modify the junctions used to 
    implement the MS-DOS device namespace.

To retrieve the current mapping for a particular MS-DOS device name or to obtain a list of all MS-DOS devices 
    known to the system, use the <a href="https://msdn.microsoft.com/ff25bc2b-dde6-40c3-a270-372daab2e5c4">QueryDosDevice</a> 
    function.

To define a drive letter assignment that is persistent across boots and not a network share, use the 
    <a href="https://msdn.microsoft.com/1535fe64-221a-4756-a9ba-81bbe7596598">SetVolumeMountPoint</a> function. If the volume to 
    be mounted already has a drive letter assigned to it, use the 
    <a href="https://msdn.microsoft.com/b1a0a273-fa7f-4794-8b50-c74f00b0228d">DeleteVolumeMountPoint</a> function to remove the 
    assignment.

Drive letters and device names defined at system boot time are protected from redefinition and deletion unless 
    the user is an administrator.

Starting with Windows XP, this function creates a device name for a caller that is not running in 
    the "LocalSystem" context in its own Local MS-DOS device namespace. If the caller  is running in 
    the "LocalSystem" context, the function creates the device name in the Global MS-DOS device 
    namespace. For more information, see 
    <a href="https://msdn.microsoft.com/7d802e9f-dc09-4e3d-b064-e9b57af396e2">Defining an MS DOS Device Name</a> and 
    <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">File Names, Paths, and Namespaces</a>.

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
No

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
No

</td>
</tr>
</table>
 

SMB does not support volume management functions. For CsvFs, a new name will not be replicated to the other nodes on the cluster.



#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/17a6df9d-07df-42f7-89c9-72a1d02141f6">Editing Drive Letter Assignments</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b1a0a273-fa7f-4794-8b50-c74f00b0228d">DeleteVolumeMountPoint</a>



<a href="https://msdn.microsoft.com/ff25bc2b-dde6-40c3-a270-372daab2e5c4">QueryDosDevice</a>



<a href="https://msdn.microsoft.com/1535fe64-221a-4756-a9ba-81bbe7596598">SetVolumeMountPoint</a>



<a href="https://msdn.microsoft.com/dc985126-970c-49f2-877f-3759125e43b6">Volume Management Functions</a>
 

 

