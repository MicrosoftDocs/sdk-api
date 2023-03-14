---
UID: NF:vds.IEnumVdsObject.Skip
title: IEnumVdsObject::Skip (vds.h)
description: The IEnumVdsObject::Skip (vds.h) method skips a specified number of objects in the enumeration.
helpviewer_keywords: ["IEnumVdsObject interface [VDS]","Skip method","IEnumVdsObject.Skip","IEnumVdsObject::Skip","Skip","Skip method [VDS]","Skip method [VDS]","IEnumVdsObject interface","base.ienumvdsobject_skip","vds/IEnumVdsObject::Skip","vdshwprv/IEnumVdsObject::Skip"]
old-location: base\ienumvdsobject_skip.htm
tech.root: base
ms.assetid: 8c0a856e-831e-489d-9e2a-bf2829bf59b6
ms.date: 08/05/2022
ms.keywords: IEnumVdsObject interface [VDS],Skip method, IEnumVdsObject.Skip, IEnumVdsObject::Skip, Skip, Skip method [VDS], Skip method [VDS],IEnumVdsObject interface, base.ienumvdsobject_skip, vds/IEnumVdsObject::Skip, vdshwprv/IEnumVdsObject::Skip
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
 - IEnumVdsObject::Skip
 - vds/IEnumVdsObject::Skip
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
 - IEnumVdsObject.Skip
---

# IEnumVdsObject::Skip


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Skips a specified number of 
   objects in the enumeration.

## -parameters

### -param celt [in]

The number of objects to skip.

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
The method skipped the specified number of objects. The number of skipped objects equals 
        <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number of objects specified is greater than the number of objects remaining. If the number of objects 
        remaining is less than the number specified in <i>celt</i>, the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ienumvdsobject-skip">Skip</a> method skips all remaining 
        objects.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>
