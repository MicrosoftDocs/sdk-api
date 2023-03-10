---
UID: NF:vdshwprv.IEnumVdsObject.Reset
title: IEnumVdsObject::Reset (vdshwprv.h)
description: The IEnumVdsObject::Reset method (vdshwprv.h) resets to the beginning of the enumeration.  
helpviewer_keywords: ["IEnumVdsObject interface [VDS]","Reset method","IEnumVdsObject.Reset","IEnumVdsObject::Reset","Reset","Reset method [VDS]","Reset method [VDS]","IEnumVdsObject interface","base.ienumvdsobject_reset","vds/IEnumVdsObject::Reset","vdshwprv/IEnumVdsObject::Reset"]
old-location: base\ienumvdsobject_reset.htm
tech.root: base
ms.assetid: cdc13cd3-bd6f-422e-89fe-244e7a7540bd
ms.date: 08/08/2022
ms.keywords: IEnumVdsObject interface [VDS],Reset method, IEnumVdsObject.Reset, IEnumVdsObject::Reset, Reset, Reset method [VDS], Reset method [VDS],IEnumVdsObject interface, base.ienumvdsobject_reset, vds/IEnumVdsObject::Reset, vdshwprv/IEnumVdsObject::Reset
req.header: vdshwprv.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumVdsObject::Reset
 - vdshwprv/IEnumVdsObject::Reset
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
 - IEnumVdsObject.Reset
---

# IEnumVdsObject::Reset


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Resets to the beginning of 
   the enumeration.



## -returns

This method can return standard HRESULT values, such as E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
The enumeration has been reset.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>
