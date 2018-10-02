---
UID: NF:vds.IVdsVolumeMF.QueryAccessPaths
title: IVdsVolumeMF::QueryAccessPaths
author: windows-sdk-content
description: Returns a list of access paths and a drive letter, if one exists, for the current volume.
old-location: base\ivdsvolumemf_queryaccesspaths.htm
tech.root: VDS
ms.assetid: 7d541245-c189-4abe-ac72-2928c7aeed95
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVdsVolumeMF interface [VDS],QueryAccessPaths method, IVdsVolumeMF.QueryAccessPaths, IVdsVolumeMF::QueryAccessPaths, QueryAccessPaths, QueryAccessPaths method [VDS], QueryAccessPaths method [VDS],IVdsVolumeMF interface, base.ivdsvolumemf_queryaccesspaths, vds/IVdsVolumeMF::QueryAccessPaths
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
 - IVdsVolumeMF.QueryAccessPaths
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsVolumeMF::QueryAccessPaths


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns a list of access paths and a drive letter, if one exists, for the current volume.


## -parameters




### -param pwszPathArray [out]

<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a>

### -param plNumberOfAccessPaths [out]

A pointer to the number of access paths on the volume.


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
The pack containing the volume is  not accessible.

</td>
</tr>
</table>
 




## -remarks



The drive letter appears as the first access path in <i>pwszPathArray</i>.




## -see-also




<a href="https://msdn.microsoft.com/4c8a63bd-ae2f-4157-92f9-aefc592c7d4f">IVdsVolumeMF</a>



<a href="https://msdn.microsoft.com/cf29639e-33fd-42f6-b616-7145521da347">IVdsVolumeMF::AddAccessPath</a>



<a href="https://msdn.microsoft.com/05020390-475f-4528-ba44-ecdfe008149f">IVdsVolumeMF::DeleteAccessPath</a>
 

 

