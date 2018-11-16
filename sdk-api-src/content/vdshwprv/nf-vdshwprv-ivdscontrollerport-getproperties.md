---
UID: NF:vdshwprv.IVdsControllerPort.GetProperties
title: IVdsControllerPort::GetProperties
author: windows-sdk-content
description: Retrieves the properties of a controller port.
old-location: base\ivdscontrollerport_getproperties.htm
tech.root: VDS
ms.assetid: 7540f2d3-c17c-4868-9e72-116219bab51c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetProperties, GetProperties method [VDS], GetProperties method [VDS],IVdsControllerPort interface, IVdsControllerPort interface [VDS],GetProperties method, IVdsControllerPort.GetProperties, IVdsControllerPort::GetProperties, base.ivdscontrollerport_getproperties, vds/IVdsControllerPort::GetProperties, vdshwprv/IVdsControllerPort::GetProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - IVdsControllerPort.GetProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vdshwprv.h
: 
- IVdsControllerPort.GetProperties
: 
---

# IVdsControllerPort::GetProperties


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Retrieves the properties of a controller port.


## -parameters




### -param pPortProp [out]

The address of a member of the <a href="https://msdn.microsoft.com/40f81f31-3776-4685-8b79-c047c669b2bb">VDS_PORT_PROP</a> 
      structure that is allocated and passed in by the caller. VDS allocates memory for the 
      <b>pwszFriendlyName</b> and <b>pwszIdentification</b> strings. Callers 
      must free the strings by using the <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> 
      function.


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The properties were successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_S_PROPERTIES_INCOMPLETE</b></b></dt>
<dt>0x00042715L</dt>
</dl>
</td>
<td width="60%">
Some but not all of the properties were successfully retrieved. Note that there are many possible reasons for failing to retrieve all properties, including device removal.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
The cache of the provider is corrupted. This indicates a software or communication problem inside a 
        provider that caches information about the attached devices. The caller can use the 
        <a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a> 
        method to restore the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_OBJECT_DELETED</b></b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
The controller port object is no longer present.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a0ceaf1d-b839-4cf7-b64e-9100f3cf23ef">IVdsControllerPort</a>



<a href="https://msdn.microsoft.com/40f81f31-3776-4685-8b79-c047c669b2bb">VDS_PORT_PROP</a>
 

 

