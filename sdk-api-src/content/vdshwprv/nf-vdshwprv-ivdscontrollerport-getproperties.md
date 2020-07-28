---
UID: NF:vdshwprv.IVdsControllerPort.GetProperties
title: IVdsControllerPort::GetProperties (vdshwprv.h)
description: Retrieves the properties of a controller port.
helpviewer_keywords: ["GetProperties","GetProperties method [VDS]","GetProperties method [VDS]","IVdsControllerPort interface","IVdsControllerPort interface [VDS]","GetProperties method","IVdsControllerPort.GetProperties","IVdsControllerPort::GetProperties","base.ivdscontrollerport_getproperties","vds/IVdsControllerPort::GetProperties","vdshwprv/IVdsControllerPort::GetProperties"]
old-location: base\ivdscontrollerport_getproperties.htm
tech.root: base
ms.assetid: 7540f2d3-c17c-4868-9e72-116219bab51c
ms.date: 12/05/2018
ms.keywords: GetProperties, GetProperties method [VDS], GetProperties method [VDS],IVdsControllerPort interface, IVdsControllerPort interface [VDS],GetProperties method, IVdsControllerPort.GetProperties, IVdsControllerPort::GetProperties, base.ivdscontrollerport_getproperties, vds/IVdsControllerPort::GetProperties, vdshwprv/IVdsControllerPort::GetProperties
f1_keywords:
- vdshwprv/IVdsControllerPort.GetProperties
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsControllerPort::GetProperties


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Retrieves the properties of a controller port.


## -parameters




### -param pPortProp [out]

The address of a member of the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_port_prop">VDS_PORT_PROP</a> 
      structure that is allocated and passed in by the caller. VDS allocates memory for the 
      <b>pwszFriendlyName</b> and <b>pwszIdentification</b> strings. Callers 
      must free the strings by using the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> 
      function.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
        <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> 
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




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdscontrollerport">IVdsControllerPort</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_port_prop">VDS_PORT_PROP</a>
 

 

