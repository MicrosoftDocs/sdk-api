---
UID: NF:vds.IVdsSubSystemInterconnect.GetSupportedInterconnects
title: IVdsSubSystemInterconnect::GetSupportedInterconnects
author: windows-sdk-content
description: Returns the interconnect types that the subsystem supports.
old-location: base\ivdssubsysteminterconnect_getsupportedinterconnects.htm
tech.root: vds
ms.assetid: 5e8e69b4-023d-49f7-a363-bae1ae9536ac
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSupportedInterconnects, GetSupportedInterconnects method, GetSupportedInterconnects method,IVdsSubSystemInterconnect interface, IVdsSubSystemInterconnect interface,GetSupportedInterconnects method, IVdsSubSystemInterconnect.GetSupportedInterconnects, IVdsSubSystemInterconnect::GetSupportedInterconnects, base.ivdssubsysteminterconnect_getsupportedinterconnects, vds/IVdsSubSystemInterconnect::GetSupportedInterconnects, vdshwprv/IVdsSubSystemInterconnect::GetSupportedInterconnects
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IVdsSubSystemInterconnect.GetSupportedInterconnects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsSubSystemInterconnect::GetSupportedInterconnects


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the interconnect types that the subsystem supports.


## -parameters




### -param pulSupportedInterconnectsFlag [out]

A pointer to a caller-allocated <b>ULONG</b> value that receives a bitmask of <a href="https://msdn.microsoft.com/ada895cb-1ff0-43df-8cd5-8ebc70cb97e2">VDS_INTERCONNECT_FLAG</a> flags, one for each interconnect type that the subsystem supports. This parameter is required and cannot be <b>NULL</b>.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The method completed successfully.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d690827a-4608-4d02-a3bb-5cdb5073b0ad">IVdsSubSystemInterconnect</a>
 

 

