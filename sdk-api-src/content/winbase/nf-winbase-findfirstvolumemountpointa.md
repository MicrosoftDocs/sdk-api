---
UID: NF:winbase.FindFirstVolumeMountPointA
title: FindFirstVolumeMountPointA function
author: windows-driver-content
description: Retrieves the name of a mounted folder on the specified volume.
old-location: fs\findfirstvolumemountpoint.htm
old-project: FileIO
ms.assetid: 2ac3c22d-b8dd-43d8-a7af-877b54e42d9d
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: FindFirstVolumeMountPoint, FindFirstVolumeMountPoint function [Files], FindFirstVolumeMountPointA, FindFirstVolumeMountPointW, _win32_findfirstvolumemountpoint, base.findfirstvolumemountpoint, fs.findfirstvolumemountpoint, winbase/FindFirstVolumeMountPoint, winbase/FindFirstVolumeMountPointA, winbase/FindFirstVolumeMountPointW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindFirstVolumeMountPointW (Unicode) and FindFirstVolumeMountPointA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
-	kernel32legacy.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
-	API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
-	FindFirstVolumeMountPoint
-	FindFirstVolumeMountPointA
-	FindFirstVolumeMountPointW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FindFirstVolumeMountPointA function


## -description


Retrieves the name of a mounted folder on the specified volume. <b>FindFirstVolumeMountPoint</b> is used to begin scanning the mounted folders on a 
    volume.


## -parameters




### -param lpszRootPathName [in]

A volume GUID path for the volume to scan for mounted folders. A trailing backslash is required.


### -param lpszVolumeMountPoint [out]

A pointer to a buffer that receives the name of the first mounted folder that is found.


### -param cchBufferLength [in]

The length of the buffer that receives the path to the mounted folder, in 
      <b>TCHAR</b>s.


## -returns



If the function succeeds, the return value is a search handle used in a subsequent call to the 
       <a href="https://msdn.microsoft.com/299e2fed-74d8-4008-b593-981c52016532">FindNextVolumeMountPoint</a> and 
       <a href="https://msdn.microsoft.com/f0f09a9d-e463-4457-9078-3d324fa8d4d6">FindVolumeMountPointClose</a> functions.

If the function fails to find a mounted folder on the volume, the return value is the 
       <b>INVALID_HANDLE_VALUE</b> error code. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>FindFirstVolumeMountPoint</b> function 
    opens a mounted folder search handle and returns information about the first mounted folder that is found on the 
    specified volume. After the search handle is established, you can use the 
    <a href="https://msdn.microsoft.com/299e2fed-74d8-4008-b593-981c52016532">FindNextVolumeMountPoint</a> function to search for 
    other mounted folders. When the search handle is no longer needed, close it with the 
    <a href="https://msdn.microsoft.com/f0f09a9d-e463-4457-9078-3d324fa8d4d6">FindVolumeMountPointClose</a> function.

The <b>FindFirstVolumeMountPoint</b>, 
    <a href="https://msdn.microsoft.com/299e2fed-74d8-4008-b593-981c52016532">FindNextVolumeMountPoint</a>, and 
    <a href="https://msdn.microsoft.com/f0f09a9d-e463-4457-9078-3d324fa8d4d6">FindVolumeMountPointClose</a> functions return 
    paths to mounted folders for a specified volume. They do not return drive letters or volume 
    <b>GUID</b> paths. For information about enumerating the volume 
    <b>GUID</b> paths for a volume, see 
    <a href="https://msdn.microsoft.com/f6590a46-2e09-472c-8231-bb24c9b0b5f6">Enumerating Volume GUID Paths</a>.

You should not assume any correlation between the order of the mounted folders that are returned by these 
    functions and the order of the mounted folders that are returned by other functions or tools.

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
 

SMB does not support volume management functions. CsvFS does not support adding mount point on a CSV volume. 
     ReFS does not index mount points.




## -see-also




<a href="https://msdn.microsoft.com/299e2fed-74d8-4008-b593-981c52016532">FindNextVolumeMountPoint</a>



<a href="https://msdn.microsoft.com/f0f09a9d-e463-4457-9078-3d324fa8d4d6">FindVolumeMountPointClose</a>



<a href="https://msdn.microsoft.com/6de526cd-5537-4411-b43f-3c0bdac70d64">Mounted Folders</a>



<a href="https://msdn.microsoft.com/dc985126-970c-49f2-877f-3759125e43b6">Volume Management Functions</a>
 

 

