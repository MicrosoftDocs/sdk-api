---
UID: NF:setupapi.SetupRemoveFromDiskSpaceListW
title: SetupRemoveFromDiskSpaceListW function
author: windows-driver-content
description: The SetupRemoveFromDiskSpaceList function removes a file delete or copy operation from a disk-space list.
old-location: setup\setupremovefromdiskspacelist.htm
old-project: SetupApi
ms.assetid: 0d23c8ce-ada6-4640-b9ad-8989f9a122a2
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: FILEOP_COPY, FILEOP_DELETE, SetupRemoveFromDiskSpaceList, SetupRemoveFromDiskSpaceList function [Setup API], SetupRemoveFromDiskSpaceListA, SetupRemoveFromDiskSpaceListW, _setupapi_setupremovefromdiskspacelist, setup.setupremovefromdiskspacelist, setupapi/SetupRemoveFromDiskSpaceList, setupapi/SetupRemoveFromDiskSpaceListA, setupapi/SetupRemoveFromDiskSpaceListW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupRemoveFromDiskSpaceListW (Unicode) and SetupRemoveFromDiskSpaceListA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Setupapi.dll
api_name:
-	SetupRemoveFromDiskSpaceList
-	SetupRemoveFromDiskSpaceListA
-	SetupRemoveFromDiskSpaceListW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# SetupRemoveFromDiskSpaceListW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupRemoveFromDiskSpaceList</b> function removes a file delete or copy operation from a disk-space list.


## -parameters




### -param DiskSpace [in]

Handle to a disk-space list.


### -param TargetFilespec [in]

Pointer to a null-terminated string that specifies the file name of the file to remove from the disk-space list. This is typically a fully qualified  path. Otherwise, the path must be relative to the current directory.


### -param Operation [in]

File operation to be removed from the list. This parameter can be one of the following values. 



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



If the file was not in the list, the 
<b>SetupRemoveFromDiskSpaceList</b> function returns a nonzero value and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INVALID_DRIVE or ERROR_INVALID_NAME. If the file was in the list then upon success the routine returns a nonzero value and 
<b>GetLastError</b> returns NO_ERROR.

If the routine fails for some other reason, it returns zero and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns extended error information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/f1bb7096-b4a6-450b-9552-9a3dc4c71f24">SetupAddToDiskSpaceList</a>



<a href="https://msdn.microsoft.com/dd104c59-faee-4eb6-abbc-a4c13d766298">SetupRemoveInstallSectionFromDiskSpaceList</a>



<a href="https://msdn.microsoft.com/0ac9becd-bdd5-4017-b880-4f226150d275">SetupRemoveSectionFromDiskSpaceList</a>
 

 

