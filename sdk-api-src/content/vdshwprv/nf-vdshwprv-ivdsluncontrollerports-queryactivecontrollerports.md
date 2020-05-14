---
UID: NF:vdshwprv.IVdsLunControllerPorts.QueryActiveControllerPorts
title: IVdsLunControllerPorts::QueryActiveControllerPorts (vdshwprv.h)
description: Returns an enumeration of currently active controller ports.helpviewer_keywords: ["IVdsLunControllerPorts interface","QueryActiveControllerPorts method","IVdsLunControllerPorts.QueryActiveControllerPorts","IVdsLunControllerPorts::QueryActiveControllerPorts","QueryActiveControllerPorts","QueryActiveControllerPorts method","QueryActiveControllerPorts method","IVdsLunControllerPorts interface","base.ivdsluncontrollerports_queryactivecontrollerports","vds/IVdsLunControllerPorts::QueryActiveControllerPorts","vdshwprv/IVdsLunControllerPorts::QueryActiveControllerPorts"]
old-location: base\ivdsluncontrollerports_queryactivecontrollerports.htm
tech.root: VDS
ms.assetid: 0a6f34c6-f333-4abf-ad37-b7756b125045
ms.date: 12/05/2018
ms.keywords: IVdsLunControllerPorts interface,QueryActiveControllerPorts method, IVdsLunControllerPorts.QueryActiveControllerPorts, IVdsLunControllerPorts::QueryActiveControllerPorts, QueryActiveControllerPorts, QueryActiveControllerPorts method, QueryActiveControllerPorts method,IVdsLunControllerPorts interface, base.ivdsluncontrollerports_queryactivecontrollerports, vds/IVdsLunControllerPorts::QueryActiveControllerPorts, vdshwprv/IVdsLunControllerPorts::QueryActiveControllerPorts
f1_keywords:
- vdshwprv/IVdsLunControllerPorts.QueryActiveControllerPorts
dev_langs:
- c++
req.header: vdshwprv.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Vds.h
- VdsHwPrv.h
api_name:
- IVdsLunControllerPorts.QueryActiveControllerPorts
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
---

# IVdsLunControllerPorts::QueryActiveControllerPorts


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an enumeration of currently active controller ports— 
    the controller ports through which the LUN can be accessed. This method replaces 
    <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-queryactivecontrollers">IVdsLun::QueryActiveControllers</a>.


## -parameters




### -param ppEnum [out]

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface pointer that can be used to enumerate the controller ports  as <a href="https://docs.microsoft.com/windows/desktop/VDS/controller-port-object">controller port objects</a>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the controller port objects when they are no longer needed by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.
     


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The enumeration of controller ports was successfully returned. If the LUN has no active controller ports, the 
        enumeration is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
The cache of the provider is corrupted. This indicates a software or communication problem inside a provider 
        that caches information about the attached devices. The caller can use the 
        <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method to 
        restore the cache.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_OBJECT_DELETED</b></b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
The LUN object is no longer present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_OBJECT_STATUS_FAILED</b></b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The LUN is in a failed state and is unable to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress. This operation cannot proceed until previous operations are complete.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-queryactivecontrollers">IVdsLun::QueryActiveControllers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsluncontrollerports">IVdsLunControllerPorts</a>
 

 

