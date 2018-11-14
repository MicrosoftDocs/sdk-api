---
UID: NF:vds.IVdsVolumeMF.GetFileSystemProperties
title: IVdsVolumeMF::GetFileSystemProperties
author: windows-sdk-content
description: Returns property details about the file system on the current volume.
old-location: base\ivdsvolumemf_getfilesystemproperties.htm
tech.root: VDS
ms.assetid: 43f5495c-5a60-44fd-b217-16464c4693a4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetFileSystemProperties, GetFileSystemProperties method [VDS], GetFileSystemProperties method [VDS],IVdsVolumeMF interface, IVdsVolumeMF interface [VDS],GetFileSystemProperties method, IVdsVolumeMF.GetFileSystemProperties, IVdsVolumeMF::GetFileSystemProperties, base.ivdsvolumemf_getfilesystemproperties, vds/IVdsVolumeMF::GetFileSystemProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsVolumeMF.GetFileSystemProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vds.h
: 
- IVdsVolumeMF.GetFileSystemProperties
: 
---

# IVdsVolumeMF::GetFileSystemProperties


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns property details about the file system on the current volume.


## -parameters




### -param pFileSystemProp [out]

The address of the <a href="https://msdn.microsoft.com/1068eb6d-0f7f-4d04-b7ec-f40e54ff8325">VDS_FILE_SYSTEM_PROP</a> 
      structure allocated and passed in by the caller. VDS allocates memory for the 
      <b>pwszLabel</b> member string. Callers must free the string by using the 
      <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_NOT_MOUNTED</b></dt>
<dt>0x8004244FL</dt>
</dl>
</td>
<td width="60%">
The volume has been taken offline.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_STATUS_FAILED</b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The volume failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PACK_OFFLINE</b></dt>
<dt>0x80042444L</dt>
</dl>
</td>
<td width="60%">
The pack containing the volume is not accessible.

</td>
</tr>
</table>
 




## -remarks



If the volume is encrypted by BitLocker, the type member of the <a href="https://msdn.microsoft.com/1068eb6d-0f7f-4d04-b7ec-f40e54ff8325">VDS_FILE_SYSTEM_PROP</a> structure will be set to <b>VDS_FST_UNKNOWN</b> on return.




## -see-also




<a href="https://msdn.microsoft.com/4c8a63bd-ae2f-4157-92f9-aefc592c7d4f">IVdsVolumeMF</a>



<a href="https://msdn.microsoft.com/1068eb6d-0f7f-4d04-b7ec-f40e54ff8325">VDS_FILE_SYSTEM_PROP</a>



<a href="https://msdn.microsoft.com/56f2d969-eb1c-44c2-8a12-077a02ae40dc">VDS_FILE_SYSTEM_TYPE</a>
 

 

