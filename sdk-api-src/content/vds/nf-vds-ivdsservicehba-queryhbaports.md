---
UID: NF:vds.IVdsServiceHba.QueryHbaPorts
title: IVdsServiceHba::QueryHbaPorts (vds.h)
description: Returns an IEnumVdsObject enumeration object containing a list of the HBA ports known to VDS on the local system.
helpviewer_keywords: ["IVdsServiceHba interface [VDS]","QueryHbaPorts method","IVdsServiceHba.QueryHbaPorts","IVdsServiceHba::QueryHbaPorts","QueryHbaPorts","QueryHbaPorts method [VDS]","QueryHbaPorts method [VDS]","IVdsServiceHba interface","base.ivdsservicehba_queryhbaports","vds/IVdsServiceHba::QueryHbaPorts"]
old-location: base\ivdsservicehba_queryhbaports.htm
tech.root: base
ms.assetid: 2f81e5e9-5563-4435-8ecb-82f2c385c3dc
ms.date: 12/05/2018
ms.keywords: IVdsServiceHba interface [VDS],QueryHbaPorts method, IVdsServiceHba.QueryHbaPorts, IVdsServiceHba::QueryHbaPorts, QueryHbaPorts, QueryHbaPorts method [VDS], QueryHbaPorts method [VDS],IVdsServiceHba interface, base.ivdsservicehba_queryhbaports, vds/IVdsServiceHba::QueryHbaPorts
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsServiceHba::QueryHbaPorts
 - vds/IVdsServiceHba::QueryHbaPorts
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vds.h
api_name:
 - IVdsServiceHba.QueryHbaPorts
---

# IVdsServiceHba::QueryHbaPorts


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> enumeration object containing 
     a list of the HBA ports known to VDS on the local system.

## -parameters

### -param ppEnum [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface pointer that can be used to enumerate the HBA ports  as <a href="/windows/desktop/VDS/startup-and-service-objects">HBA port objects</a>. For more information, see <a href="/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the HBA port objects when they are no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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
The enumeration of HBA ports was returned successfully. If the local system has no HBA ports, the enumeration 
        is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INITIALIZED_FAILED</b></dt>
<dt>0x80042401L</dt>
</dl>
</td>
<td width="60%">
VDS failed to initialize. If an application calls this method before the VDS service finishes initializing, 
        the method is blocked until the initialization is complete. If the initialization fails, this error is returned.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsservicehba">IVdsServiceHba</a>