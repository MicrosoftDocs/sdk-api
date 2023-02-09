---
UID: NF:vdshwprv.IVdsProviderPrivate.GetObject
title: IVdsProviderPrivate::GetObject (vdshwprv.h)
description: Returns the specified object.
helpviewer_keywords: ["GetObject","GetObject method [VDS]","GetObject method [VDS]","IVdsProviderPrivate interface","IVdsProviderPrivate interface [VDS]","GetObject method","IVdsProviderPrivate.GetObject","IVdsProviderPrivate::GetObject","base.ivdsproviderprivate_getobject","vdshwprv/IVdsProviderPrivate::GetObject"]
old-location: base\ivdsproviderprivate_getobject.htm
tech.root: base
ms.assetid: 3f346255-c5c6-4ca3-9718-0347c3f8294a
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject method [VDS], GetObject method [VDS],IVdsProviderPrivate interface, IVdsProviderPrivate interface [VDS],GetObject method, IVdsProviderPrivate.GetObject, IVdsProviderPrivate::GetObject, base.ivdsproviderprivate_getobject, vdshwprv/IVdsProviderPrivate::GetObject
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
 - IVdsProviderPrivate::GetObject
 - vdshwprv/IVdsProviderPrivate::GetObject
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
 - IVdsProviderPrivate.GetObject
---

# IVdsProviderPrivate::GetObject


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the specified object.

## -parameters

### -param ObjectId [in]

The GUID of the object.

### -param type [in]

The object type enumerated by <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_object_type">VDS_OBJECT_TYPE</a>.

### -param ppObjectUnk [out]

The address of an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer for the object. When the pointer is no longer needed, the caller should release it by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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
<dt><b>VDS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042405L</dt>
</dl>
</td>
<td width="60%">
The object was not found.

</td>
</tr>
</table>

## -remarks

The object can be a  subsystem, controller, LUN, LUN plex, drive, pack, disk, volume, or volume plex object. Each object represents a physical device (such as a subsystem, drive, or controllers) or a virtual device (such as a LUN or LUN plex). The hardware provider should create one COM object for each physical or virtual device.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsproviderprivate">IVdsProviderPrivate</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_object_type">VDS_OBJECT_TYPE</a>