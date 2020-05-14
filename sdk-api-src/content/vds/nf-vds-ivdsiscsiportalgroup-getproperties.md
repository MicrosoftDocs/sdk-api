---
UID: NF:vds.IVdsIscsiPortalGroup.GetProperties
title: IVdsIscsiPortalGroup::GetProperties (vds.h)
description: Returns the properties of a portal group.helpviewer_keywords: ["GetProperties","GetProperties method [VDS]","GetProperties method [VDS]","IVdsIscsiPortalGroup interface","IVdsIscsiPortalGroup interface [VDS]","GetProperties method","IVdsIscsiPortalGroup.GetProperties","IVdsIscsiPortalGroup::GetProperties","base.ivdsiscsiportalgroup_getproperties","vds/IVdsIscsiPortalGroup::GetProperties","vdshwprv/IVdsIscsiPortalGroup::GetProperties"]
old-location: base\ivdsiscsiportalgroup_getproperties.htm
tech.root: VDS
ms.assetid: 7257101e-04a5-41d5-b4fa-401106610dcf
ms.date: 12/05/2018
ms.keywords: GetProperties, GetProperties method [VDS], GetProperties method [VDS],IVdsIscsiPortalGroup interface, IVdsIscsiPortalGroup interface [VDS],GetProperties method, IVdsIscsiPortalGroup.GetProperties, IVdsIscsiPortalGroup::GetProperties, base.ivdsiscsiportalgroup_getproperties, vds/IVdsIscsiPortalGroup::GetProperties, vdshwprv/IVdsIscsiPortalGroup::GetProperties
f1_keywords:
- vds/IVdsIscsiPortalGroup.GetProperties
dev_langs:
- c++
req.header: vds.h
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
- IVdsIscsiPortalGroup.GetProperties
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
---

# IVdsIscsiPortalGroup::GetProperties


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the properties of a portal group.


## -parameters




### -param pPortalGroupProp [out]

The address of a <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_portalgroup_prop">VDS_ISCSI_PORTALGROUP_PROP</a> 
      structure allocated and passed in by the caller.


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
The properties were returned successfully.

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
The cache of the provider is corrupted. This indicates a software or communication problem inside a provider 
        that caches information about the attached devices. The caller can use the 
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
The portal group object is no longer present.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsiportalgroup">IVdsIscsiPortalGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_portalgroup_prop">VDS_ISCSI_PORTALGROUP_PROP</a>
 

 

