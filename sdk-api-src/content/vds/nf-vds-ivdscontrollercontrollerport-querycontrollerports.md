---
UID: NF:vds.IVdsControllerControllerPort.QueryControllerPorts
title: IVdsControllerControllerPort::QueryControllerPorts (vds.h)
description: The IVdsControllerControllerPort::QueryControllerPorts (vds.h) method returns an IEnumVdsObject object that enumerates the ports of the controller.
helpviewer_keywords: ["IVdsControllerControllerPort interface [VDS]","QueryControllerPorts method","IVdsControllerControllerPort.QueryControllerPorts","IVdsControllerControllerPort::QueryControllerPorts","QueryControllerPorts","QueryControllerPorts method [VDS]","QueryControllerPorts method [VDS]","IVdsControllerControllerPort interface","base.ivdscontrollercontrollerport_querycontrollerports","vds/IVdsControllerControllerPort::QueryControllerPorts","vdshwprv/IVdsControllerControllerPort::QueryControllerPorts"]
old-location: base\ivdscontrollercontrollerport_querycontrollerports.htm
tech.root: base
ms.assetid: 676d0ae9-7d9e-4dc3-93c2-56c96a05ac0a
ms.date: 08/05/2022
ms.keywords: IVdsControllerControllerPort interface [VDS],QueryControllerPorts method, IVdsControllerControllerPort.QueryControllerPorts, IVdsControllerControllerPort::QueryControllerPorts, QueryControllerPorts, QueryControllerPorts method [VDS], QueryControllerPorts method [VDS],IVdsControllerControllerPort interface, base.ivdscontrollercontrollerport_querycontrollerports, vds/IVdsControllerControllerPort::QueryControllerPorts, vdshwprv/IVdsControllerControllerPort::QueryControllerPorts
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
 - IVdsControllerControllerPort::QueryControllerPorts
 - vds/IVdsControllerControllerPort::QueryControllerPorts
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - IVdsControllerControllerPort.QueryControllerPorts
---

# IVdsControllerControllerPort::QueryControllerPorts


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> object that 
    enumerates the ports of the controller.

## -parameters

### -param ppEnum [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface pointer that can be used to enumerate the controller ports  as <a href="/windows/desktop/VDS/controller-port-object">controller port objects</a>. For more information, see <a href="/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the controller port objects when they are no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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
The enumeration of controller ports was returned successfully. If the controller has no ports, the 
        enumeration is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
The cache of the provider is corrupted. This indicates a software or communication problem inside a 
        provider that caches information about the attached devices. The caller can use the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method to 
        restore the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_DELETED</b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
The controller object is no longer present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_STATUS_FAILED</b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The controller is in a failed state and is unable to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress. This operation cannot proceed until previous operations are complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
This operation is not supported by this provider.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdscontrollercontrollerport">IVdsControllerControllerPort</a>
