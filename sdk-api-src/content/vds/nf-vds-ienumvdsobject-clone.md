---
UID: NF:vds.IEnumVdsObject.Clone
title: IEnumVdsObject::Clone (vds.h)
description: The IEnumVdsObject::Clone (vds.h) method creates an enumeration with the same state as the current enumeration.
helpviewer_keywords: ["Clone","Clone method [VDS]","Clone method [VDS]","IEnumVdsObject interface","IEnumVdsObject interface [VDS]","Clone method","IEnumVdsObject.Clone","IEnumVdsObject::Clone","base.ienumvdsobject_clone","vds/IEnumVdsObject::Clone","vdshwprv/IEnumVdsObject::Clone"]
old-location: base\ienumvdsobject_clone.htm
tech.root: base
ms.assetid: 9d547011-2200-43fc-a8de-9b90ba94c39e
ms.date: 08/05/2022
ms.keywords: Clone, Clone method [VDS], Clone method [VDS],IEnumVdsObject interface, IEnumVdsObject interface [VDS],Clone method, IEnumVdsObject.Clone, IEnumVdsObject::Clone, base.ienumvdsobject_clone, vds/IEnumVdsObject::Clone, vdshwprv/IEnumVdsObject::Clone
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumVdsObject::Clone
 - vds/IEnumVdsObject::Clone
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
 - IEnumVdsObject.Clone
---

# IEnumVdsObject::Clone


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Creates an enumeration 
   with the same state as the current enumeration.

## -parameters

### -param ppEnum [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> pointer, which 
      VDS initializes on return. Callers must release the interface.

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
The new enumeration has been created.

</td>
</tr>
</table>

## -remarks

This method enables you to record a point in an enumeration and return to that point later. When the new, 
    cloned enumeration is returned, it is at the same point in the enumeration sequence as the original. Henceforth, 
    however, the clone and the original enumeration operate independently.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>
