---
UID: NF:vds.IVdsLunControllerPorts.AssociateControllerPorts
title: IVdsLunControllerPorts::AssociateControllerPorts (vds.h)
description: The IVdsLunControllerPorts::AssociateControllerPorts method (vds.h) sets the subsystem controller ports to active or inactive with respect to the LUN. 
helpviewer_keywords: ["AssociateControllerPorts","AssociateControllerPorts method [VDS]","AssociateControllerPorts method [VDS]","IVdsLunControllerPorts interface","IVdsLunControllerPorts interface [VDS]","AssociateControllerPorts method","IVdsLunControllerPorts.AssociateControllerPorts","IVdsLunControllerPorts::AssociateControllerPorts","base.ivdsluncontrollerports_associatecontrollerports","vds/IVdsLunControllerPorts::AssociateControllerPorts","vdshwprv/IVdsLunControllerPorts::AssociateControllerPorts"]
old-location: base\ivdsluncontrollerports_associatecontrollerports.htm
tech.root: base
ms.assetid: 3b889cb7-92e4-4c18-b9b9-768865895595
ms.date: 08/05/2022
ms.keywords: AssociateControllerPorts, AssociateControllerPorts method [VDS], AssociateControllerPorts method [VDS],IVdsLunControllerPorts interface, IVdsLunControllerPorts interface [VDS],AssociateControllerPorts method, IVdsLunControllerPorts.AssociateControllerPorts, IVdsLunControllerPorts::AssociateControllerPorts, base.ivdsluncontrollerports_associatecontrollerports, vds/IVdsLunControllerPorts::AssociateControllerPorts, vdshwprv/IVdsLunControllerPorts::AssociateControllerPorts
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
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - IVdsLunControllerPorts::AssociateControllerPorts
 - vds/IVdsLunControllerPorts::AssociateControllerPorts
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
 - IVdsLunControllerPorts.AssociateControllerPorts
---

# IVdsLunControllerPorts::AssociateControllerPorts


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets the subsystem controller ports to active or inactive with respect to the LUN. This method 
    replaces <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-associatecontrollers">IVdsLun::AssociateControllers</a>.

## -parameters

### -param pActiveControllerPortIdArray

A pointer to an array of controller port GUIDs. The provider sets these controller ports to active. This array 
      includes controller ports already set to active that are to remain active.

### -param lNumberOfActiveControllerPorts

The number of controller ports specified in the  <i>pActiveControllerPortIdArray</i> parameter.

### -param pInactiveControllerPortIdArray

A
      pointer to an array of controller port GUIDs. The provider sets these controller ports to inactive. This array 
      includes controller ports already set to inactive that are to remain inactive.

### -param lNumberOfInactiveControllerPorts

The number of controller ports specified in the  <i>pInactiveControllerPortIdArray</i> parameter.

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
The association name was successfully set.

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
The cache of the provider is corrupted. This indicates a software or communication problem inside a provider 
        that caches information about the attached devices. The caller can use the 
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
The LUN object is no longer present.

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
The LUN is in a failed state and is unable to perform the requested operation.

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
<dt><b>VDS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042405L</dt>
</dl>
</td>
<td width="60%">
One or more GUIDs of data type <b>VDS_OBJECT_ID</b> specified in 
        the <i>pActiveControllerPortIdArray</i> or 
        <i>pInactiveControllerPortIdArray</i> parameters do not refer to an existing object.

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
This operation or combination of parameters is not supported by this provider.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsluncontrollerports">IVdsLunControllerPorts</a>
