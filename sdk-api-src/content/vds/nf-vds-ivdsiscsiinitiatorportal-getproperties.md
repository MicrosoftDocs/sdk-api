---
UID: NF:vds.IVdsIscsiInitiatorPortal.GetProperties
title: IVdsIscsiInitiatorPortal::GetProperties (vds.h)
description: Returns the properties of an initiator portal.
helpviewer_keywords: ["GetProperties","GetProperties method [VDS]","GetProperties method [VDS]","IVdsIscsiInitiatorPortal interface","IVdsIscsiInitiatorPortal interface [VDS]","GetProperties method","IVdsIscsiInitiatorPortal.GetProperties","IVdsIscsiInitiatorPortal::GetProperties","base.ivdsiscsiinitiatorportal_getproperties","vds/IVdsIscsiInitiatorPortal::GetProperties"]
old-location: base\ivdsiscsiinitiatorportal_getproperties.htm
tech.root: base
ms.assetid: 7bf00853-ca26-40b4-a09a-dcb5e7e08f49
ms.date: 12/05/2018
ms.keywords: GetProperties, GetProperties method [VDS], GetProperties method [VDS],IVdsIscsiInitiatorPortal interface, IVdsIscsiInitiatorPortal interface [VDS],GetProperties method, IVdsIscsiInitiatorPortal.GetProperties, IVdsIscsiInitiatorPortal::GetProperties, base.ivdsiscsiinitiatorportal_getproperties, vds/IVdsIscsiInitiatorPortal::GetProperties
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
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - IVdsIscsiInitiatorPortal::GetProperties
 - vds/IVdsIscsiInitiatorPortal::GetProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsIscsiInitiatorPortal.GetProperties
---

# IVdsIscsiInitiatorPortal::GetProperties


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the properties of an initiator portal.

## -parameters

### -param pInitiatorPortalProp [out]

The address of a 
      <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_initiator_portal_prop">VDS_ISCSI_INITIATOR_PORTAL_PROP</a> 
      structure allocated by the caller.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
The properties were returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_PROPERTIES_INCOMPLETE</b></dt>
<dt>0x00042715L</dt>
</dl>
</td>
<td width="60%">
Some but not all of the properties were successfully retrieved. Note that there are many possible reasons for failing to retrieve all properties, including device removal.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsiscsiinitiatorportal">IVdsIscsiInitiatorPortal</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_initiator_portal_prop">VDS_ISCSI_INITIATOR_PORTAL_PROP</a>