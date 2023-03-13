---
UID: NF:vds.IVdsRemovable.Eject
title: IVdsRemovable::Eject (vds.h)
description: Ejects the media from the current device.
helpviewer_keywords: ["Eject","Eject method [VDS]","Eject method [VDS]","IVdsRemovable interface","IVdsRemovable interface [VDS]","Eject method","IVdsRemovable.Eject","IVdsRemovable::Eject","base.ivdsremovable_eject","vds/IVdsRemovable::Eject"]
old-location: base\ivdsremovable_eject.htm
tech.root: base
ms.assetid: c77885bd-67af-41c1-9190-e0148c7b7ed5
ms.date: 12/05/2018
ms.keywords: Eject, Eject method [VDS], Eject method [VDS],IVdsRemovable interface, IVdsRemovable interface [VDS],Eject method, IVdsRemovable.Eject, IVdsRemovable::Eject, base.ivdsremovable_eject, vds/IVdsRemovable::Eject
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
 - IVdsRemovable::Eject
 - vds/IVdsRemovable::Eject
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
 - IVdsRemovable.Eject
---

# IVdsRemovable::Eject


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Ejects the media from the current device.



## -returns

This method can return standard HRESULT values, such as E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
The media was ejected successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DEVICE_IN_USE</b></dt>
<dt>0x80042413L</dt>
</dl>
</td>
<td width="60%">
The call to the device failed because the device was performing another operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsremovable">IVdsRemovable</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsremovable-querymedia">IVdsRemovable::QueryMedia</a>
