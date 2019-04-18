---
UID: NF:dskquota.IDiskQuotaControl.Initialize
title: IDiskQuotaControl::Initialize (dskquota.h)
author: windows-sdk-content
description: Initializes a new DiskQuotaControl object by opening the NTFS file system volume with the requested access rights.
old-location: fs\idiskquotacontrol_initialize.htm
tech.root: FileIO
ms.assetid: 352485fd-4ce7-435b-b8c2-81458786eb44
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDiskQuotaControl interface [Files],Initialize method, IDiskQuotaControl.Initialize, IDiskQuotaControl::Initialize, Initialize, Initialize method [Files], Initialize method [Files],IDiskQuotaControl interface, _win32_idiskquotacontrol_initialize, base.idiskquotacontrol_initialize, dskquota/IDiskQuotaControl::Initialize, fs.idiskquotacontrol_initialize
ms.topic: method
req.header: dskquota.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Dskquota.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dskquota.dll
api_name:
 - IDiskQuotaControl.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiskQuotaControl::Initialize


## -description


Initializes a new <b>DiskQuotaControl</b> object by opening the NTFS file system volume with the requested access rights. The return value indicates whether the volume supports NTFS file system disk quotas and whether the caller has sufficient access rights.


## -parameters




### -param pszPath [in]

The path to the volume root, such as C:\ or \\<i>yourcomputer</i>.


### -param bReadWrite [in]

If this value is <b>TRUE</b>, the volume is opened in read/write mode. If this value is <b>FALSE</b>, the volume is opened in read-only mode. To write data to the quota file, you must specify <b>TRUE</b>, and the call to this method must return successfully.


## -returns



This method returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller has insufficient access rights.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_PATHNAME</b></dt>
</dl>
</td>
<td width="60%">
The requested path name is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The requested file or object is not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The controller object has already been initialized. Multiple initialization is not allowed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The requested file path is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The file system does not support quotas.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATH_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The requested file path is not found.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>



<a href="https://msdn.microsoft.com/fa34786c-af82-4b59-bf36-e9a95a2f913e">GetVolumePathName</a>



<a href="https://msdn.microsoft.com/fc9add5a-c9ef-462d-8125-128d48018717">IDiskQuotaControl</a>
 

 

