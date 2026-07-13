---
UID: NF:vds.IVdsIscsiInitiatorPortal.GetInitiatorAdapter
title: IVdsIscsiInitiatorPortal::GetInitiatorAdapter (vds.h)
description: Returns the initiator adapter to which the initiator portal belongs.
helpviewer_keywords: ["GetInitiatorAdapter","GetInitiatorAdapter method [VDS]","GetInitiatorAdapter method [VDS]","IVdsIscsiInitiatorPortal interface","IVdsIscsiInitiatorPortal interface [VDS]","GetInitiatorAdapter method","IVdsIscsiInitiatorPortal.GetInitiatorAdapter","IVdsIscsiInitiatorPortal::GetInitiatorAdapter","base.ivdsiscsiinitiatorportal_getinitiatoradapter","vds/IVdsIscsiInitiatorPortal::GetInitiatorAdapter"]
old-location: base\ivdsiscsiinitiatorportal_getinitiatoradapter.htm
tech.root: base
ms.assetid: fcdd2083-36e0-4924-9af0-87a9fe4711e0
ms.date: 12/05/2018
ms.keywords: GetInitiatorAdapter, GetInitiatorAdapter method [VDS], GetInitiatorAdapter method [VDS],IVdsIscsiInitiatorPortal interface, IVdsIscsiInitiatorPortal interface [VDS],GetInitiatorAdapter method, IVdsIscsiInitiatorPortal.GetInitiatorAdapter, IVdsIscsiInitiatorPortal::GetInitiatorAdapter, base.ivdsiscsiinitiatorportal_getinitiatoradapter, vds/IVdsIscsiInitiatorPortal::GetInitiatorAdapter
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
 - IVdsIscsiInitiatorPortal::GetInitiatorAdapter
 - vds/IVdsIscsiInitiatorPortal::GetInitiatorAdapter
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
 - IVdsIscsiInitiatorPortal.GetInitiatorAdapter
---

# IVdsIscsiInitiatorPortal::GetInitiatorAdapter


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the initiator adapter to which the initiator portal belongs.

## -parameters

### -param ppInitiatorAdapter [out]

The address of an <a href="/windows/desktop/api/vds/nn-vds-ivdsiscsiinitiatoradapter">IVdsIscsiInitiatorAdapter</a> 
      interface pointer. VDS initializes the interface on return. Callers must release the interface.

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
The initiator adapter was returned successfully.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsiscsiinitiatoradapter">IVdsIscsiInitiatorAdapter</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsiscsiinitiatorportal">IVdsIscsiInitiatorPortal</a>