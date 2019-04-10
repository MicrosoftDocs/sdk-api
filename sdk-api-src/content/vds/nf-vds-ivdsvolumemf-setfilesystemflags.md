---
UID: NF:vds.IVdsVolumeMF.SetFileSystemFlags
title: IVdsVolumeMF::SetFileSystemFlags (vds.h)
author: windows-sdk-content
description: Sets the file-system flags.
old-location: base\ivdsvolumemf_setfilesystemflags.htm
tech.root: VDS
ms.assetid: 836f4a8d-8736-4876-8de3-a6265d7eb66a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsVolumeMF interface [VDS],SetFileSystemFlags method, IVdsVolumeMF.SetFileSystemFlags, IVdsVolumeMF::SetFileSystemFlags, SetFileSystemFlags, SetFileSystemFlags method [VDS], SetFileSystemFlags method [VDS],IVdsVolumeMF interface, base.ivdsvolumemf_setfilesystemflags, vds/IVdsVolumeMF::SetFileSystemFlags
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
 - IVdsVolumeMF.SetFileSystemFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsVolumeMF::SetFileSystemFlags


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Sets the file-system flags.


## -parameters




### -param ulFlags [in]

The flags enumerated by <a href="https://msdn.microsoft.com/2598877b-03f0-4190-8dcc-41ea3cb9497f">VDS_FILE_SYSTEM_FLAG</a>. Callers can set the <b>VDS_FPF_COMPRESSED</b> flag.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
<dt><b>VDS_E_INVALID_OPERATION</b></dt>
<dt>0x80042415L</dt>
</dl>
</td>
<td width="60%">
The volume is hidden. This method cannot be called on a hidden volume.

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
 




## -see-also




<a href="https://msdn.microsoft.com/4c8a63bd-ae2f-4157-92f9-aefc592c7d4f">IVdsVolumeMF</a>



<a href="https://msdn.microsoft.com/f3b02b4a-109c-419f-94c1-fc2f15ea5291">IVdsVolumeMF::ClearFileSystemFlags</a>
 

 

