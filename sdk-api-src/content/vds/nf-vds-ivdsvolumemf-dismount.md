---
UID: NF:vds.IVdsVolumeMF.Dismount
title: IVdsVolumeMF::Dismount
author: windows-sdk-content
description: Dismounts a mounted volume.
old-location: base\ivdsvolumemf_dismount.htm
tech.root: vds
ms.assetid: 1ef5a1e6-0e41-4077-9ae8-fe266f2623cc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Dismount, Dismount method [VDS], Dismount method [VDS],IVdsVolumeMF interface, IVdsVolumeMF interface [VDS],Dismount method, IVdsVolumeMF.Dismount, IVdsVolumeMF::Dismount, base.ivdsvolumemf_dismount, vds/IVdsVolumeMF::Dismount
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
 - IVdsVolumeMF.Dismount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsVolumeMF::Dismount


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Dismounts a mounted volume.


## -parameters




### -param bForce [in]

If <b>TRUE</b>, the volume is dismounted even if it is in use; otherwise, the operation fails if the volume is in use.


### -param bPermanent [in]

If <b>TRUE</b>, the volume remains dismounted until an access path is added.


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
<dt><b>VDS_E_VOLUME_TEMPORARILY_DISMOUNTED</b></dt>
<dt>0x8004245CL</dt>
</dl>
</td>
<td width="60%">
The volume is already dismounted. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
The volume cannot be dismounted. It does not support the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_PERMANENTLY_DISMOUNTED</b></dt>
<dt>0x8004245DL</dt>
</dl>
</td>
<td width="60%">
The volume is already dismounted. It cannot be dismounted temporarily until it becomes mountable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_HAS_PATH</b></dt>
<dt>0x8004245EL</dt>
</dl>
</td>
<td width="60%">
The volume cannot be dismounted because it still has an access path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DEVICE_IN_USE</b></dt>
<dt>0x80042413L</dt>
</dl>
</td>
<td width="60%">
The volume is in use and cannot be dismounted.

</td>
</tr>
</table>
 




## -remarks



 To mount a volume, use the <a href="https://msdn.microsoft.com/1de3bbd7-cd81-42f9-9e25-48a0a07e9ccc">Mount</a> method.




## -see-also




<a href="https://msdn.microsoft.com/4c8a63bd-ae2f-4157-92f9-aefc592c7d4f">IVdsVolumeMF</a>



<a href="https://msdn.microsoft.com/1de3bbd7-cd81-42f9-9e25-48a0a07e9ccc">IVdsVolumeMF::Mount</a>
 

 

