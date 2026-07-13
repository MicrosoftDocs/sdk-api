---
UID: NF:vds.IVdsIscsiInitiatorAdapter.QueryInitiatorPortals
title: IVdsIscsiInitiatorAdapter::QueryInitiatorPortals (vds.h)
description: Returns an object that enumerates the iSCSI initiator portals of the initiator adapter.
helpviewer_keywords: ["IVdsIscsiInitiatorAdapter interface [VDS]","QueryInitiatorPortals method","IVdsIscsiInitiatorAdapter.QueryInitiatorPortals","IVdsIscsiInitiatorAdapter::QueryInitiatorPortals","QueryInitiatorPortals","QueryInitiatorPortals method [VDS]","QueryInitiatorPortals method [VDS]","IVdsIscsiInitiatorAdapter interface","base.ivdsiscsiinitiatoradapter_queryinitiatorportals","vds/IVdsIscsiInitiatorAdapter::QueryInitiatorPortals"]
old-location: base\ivdsiscsiinitiatoradapter_queryinitiatorportals.htm
tech.root: base
ms.assetid: d3c893c0-167f-46f5-92f8-aa61f5e16542
ms.date: 12/05/2018
ms.keywords: IVdsIscsiInitiatorAdapter interface [VDS],QueryInitiatorPortals method, IVdsIscsiInitiatorAdapter.QueryInitiatorPortals, IVdsIscsiInitiatorAdapter::QueryInitiatorPortals, QueryInitiatorPortals, QueryInitiatorPortals method [VDS], QueryInitiatorPortals method [VDS],IVdsIscsiInitiatorAdapter interface, base.ivdsiscsiinitiatoradapter_queryinitiatorportals, vds/IVdsIscsiInitiatorAdapter::QueryInitiatorPortals
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
 - IVdsIscsiInitiatorAdapter::QueryInitiatorPortals
 - vds/IVdsIscsiInitiatorAdapter::QueryInitiatorPortals
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
 - IVdsIscsiInitiatorAdapter.QueryInitiatorPortals
---

# IVdsIscsiInitiatorAdapter::QueryInitiatorPortals


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an object that enumerates the iSCSI initiator portals of  the initiator adapter.

## -parameters

### -param ppEnum [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface pointer that can be used to enumerate the  initiator portals  as <a href="/windows/desktop/VDS/startup-and-service-objects">initiator portal objects</a>. For more information, see <a href="/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the initiator portal objects when they are no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
The enumeration of initiator portals was successfully returned. If the initiator adapter has no portals, the 
        enumeration is empty.
       

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsiscsiinitiatoradapter">IVdsIscsiInitiatorAdapter</a>