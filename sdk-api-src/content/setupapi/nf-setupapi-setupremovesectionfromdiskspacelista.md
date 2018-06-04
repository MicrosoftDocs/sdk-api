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

# SetupRemoveSectionFromDiskSpaceListA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupRemoveSectionFromDiskSpaceList</b> function removes the file delete or copy operations listed in a <b>Copy Files</b> section of an INF file from a disk-space list.


## -parameters




### -param DiskSpace [in]

Handle to the disk-space list.


### -param InfHandle [in]

Handle to an open INF file that contains the <b>SourceDisksFiles</b> section. If <i>ListInfHandle</i> is not specified, this INF file must also contain the section specified by <i>SectionName</i>.


### -param ListInfHandle [in]

Optional handle to an open INF file that contains the section to remove from the disk-space list. Otherwise, <i>InfHandle</i> must contain the section specified by <i>SectionName</i>.


### -param SectionName [in]

Pointer to a null-terminated string that specifies the name of the <b>Copy Files</b> or <b>Delete Files</b> section to remove from the disk-space list.


### -param Operation [in]

File operation to remove from the list. This parameter can be one of the following values. 



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
<td width="40%"><a id="FILEOP_COPY"></a><a id="fileop_copy"></a><dl>
<dt><b>FILEOP_COPY</b></dt>
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




## -remarks



The file operations removed by the 
<b>SetupRemoveSectionFromDiskSpaceList</b> function are typically those that have been added to the list by using the 
<a href="https://msdn.microsoft.com/8225d0b4-b750-4580-83f5-dcffdf2ee67b">SetupAddSectionToDiskSpaceList</a> function, though this is not a requirement. The 
<b>SetupRemoveSectionFromDiskSpaceList</b> function ignores files in the INF section that are not listed in the disk-space list.

This function requires a Windows INF file. Some older INF file  formats may not be supported. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/8225d0b4-b750-4580-83f5-dcffdf2ee67b">SetupAddSectionToDiskSpaceList</a>



<a href="https://msdn.microsoft.com/0d23c8ce-ada6-4640-b9ad-8989f9a122a2">SetupRemoveFromDiskSpaceList</a>



<a href="https://msdn.microsoft.com/dd104c59-faee-4eb6-abbc-a4c13d766298">SetupRemoveInstallSectionFromDiskSpaceList</a>
 

 

