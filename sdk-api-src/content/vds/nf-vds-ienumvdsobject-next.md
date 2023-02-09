---
UID: NF:vds.IEnumVdsObject.Next
title: IEnumVdsObject::Next (vds.h)
description: The IEnumVdsObject::Next (vds.h) method returns a specified number of objects in the enumeration, beginning from the current point.
helpviewer_keywords: ["IEnumVdsObject interface [VDS]","Next method","IEnumVdsObject.Next","IEnumVdsObject::Next","Next","Next method [VDS]","Next method [VDS]","IEnumVdsObject interface","base.ienumvdsobject_next","vds/IEnumVdsObject::Next","vdshwprv/IEnumVdsObject::Next"]
old-location: base\ienumvdsobject_next.htm
tech.root: base
ms.assetid: 372eff29-7481-45aa-ad66-73147f7a631f
ms.date: 08/05/2022
ms.keywords: IEnumVdsObject interface [VDS],Next method, IEnumVdsObject.Next, IEnumVdsObject::Next, Next, Next method [VDS], Next method [VDS],IEnumVdsObject interface, base.ienumvdsobject_next, vds/IEnumVdsObject::Next, vdshwprv/IEnumVdsObject::Next
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
 - IEnumVdsObject::Next
 - vds/IEnumVdsObject::Next
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
 - IEnumVdsObject.Next
---

# IEnumVdsObject::Next


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns a specified number of 
   objects in the enumeration, beginning from the current point. For more information, see <a href="/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>.

## -parameters

### -param celt [in]

The number of objects to return.

### -param ppObjectArray [out]

The address of an array of <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointers, which VDS initializes 
      on return.

### -param pcFetched [out]

The address of a <b>ULONG</b>, which VDS initializes on return to the number of 
      objects in <i>ppObjectArray</i>.

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
The method returned the specified number of objects. The number of returned objects reported in 
        <i>pcFetched</i> equals <i>celt</i>; returns those objects.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified number of returned objects is greater than the number of objects remaining. All remaining 
        objects are returned, and the number of returned objects is reported in <i>pcFetched</i> is 
        less than <i>celt</i>; returns those objects.

</td>
</tr>
</table>

## -remarks

To obtain object-specific interface pointers from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointers returned in the <i>ppObjectArray</i> array, use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>
