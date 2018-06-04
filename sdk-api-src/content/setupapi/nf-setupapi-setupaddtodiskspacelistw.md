---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SetupAddToDiskSpaceListW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupAddToDiskSpaceList</b> function adds a single delete or copy operation to a disk-space list. To add all the file operations in a section of an INF file, use either 
<a href="https://msdn.microsoft.com/8225d0b4-b750-4580-83f5-dcffdf2ee67b">SetupAddSectionToDiskSpaceList</a>, or 
<a href="https://msdn.microsoft.com/322f36d7-a683-4a48-b294-393277f09e7d">SetupAddInstallSectionToDiskSpaceList</a>.

Target disk compression is ignored by this function. Files are assumed to occupy their full size on the target disk.


## -parameters




### -param DiskSpace [in]

Handle to the disk-space list.


### -param TargetFilespec [in]

File name of the file to be added to the disk-space list. You should use a null-terminated string that specifies  a fully qualified path. Otherwise, the path must be relative to the current directory.


### -param FileSize [in]

Uncompressed size of the file as it will exist in the target directory, in bytes. You can use 
<a href="https://msdn.microsoft.com/f1db8ad5-b133-410e-9843-38b09e2ef5e7">SetupGetSourceFileSize</a> to retrieve this information from an INF file. This parameter is ignored for FILEOP_DELETE operations.


### -param Operation [in]

File operation to be added to the list. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILEOP_DELETE"></a><a id="fileop_delete"></a><dl>
<dt><b>FILEOP_DELETE</b></dt>
</dl>
</td>
<td width="60%">
A file delete operation.

</td>
</tr>
<tr>
<td width="40%"><a id="FILEOP_COPY."></a><a id="fileop_copy."></a><dl>
<dt><b>FILEOP_COPY.</b></dt>
</dl>
</td>
<td width="60%">
A file copy operation.

</td>
</tr>
</table>
 


### -param Reserved1 [in]

Must be zero.


### -param Reserved2 [in]

Must be zero.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>
 

 

