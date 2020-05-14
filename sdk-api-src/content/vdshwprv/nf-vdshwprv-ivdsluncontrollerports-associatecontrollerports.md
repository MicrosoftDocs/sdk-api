---
UID: NF:vdshwprv.IVdsLunControllerPorts.AssociateControllerPorts
title: IVdsLunControllerPorts::AssociateControllerPorts (vdshwprv.h)
description: Sets the subsystem controller ports to active or inactive with respect to the LUN. This method replaces IVdsLun::AssociateControllers.helpviewer_keywords: ["AssociateControllerPorts","AssociateControllerPorts method [VDS]","AssociateControllerPorts method [VDS]","IVdsLunControllerPorts interface","IVdsLunControllerPorts interface [VDS]","AssociateControllerPorts method","IVdsLunControllerPorts.AssociateControllerPorts","IVdsLunControllerPorts::AssociateControllerPorts","base.ivdsluncontrollerports_associatecontrollerports","vds/IVdsLunControllerPorts::AssociateControllerPorts","vdshwprv/IVdsLunControllerPorts::AssociateControllerPorts"]
old-location: base\ivdsluncontrollerports_associatecontrollerports.htm
tech.root: VDS
ms.assetid: 3b889cb7-92e4-4c18-b9b9-768865895595
ms.date: 12/05/2018
ms.keywords: AssociateControllerPorts, AssociateControllerPorts method [VDS], AssociateControllerPorts method [VDS],IVdsLunControllerPorts interface, IVdsLunControllerPorts interface [VDS],AssociateControllerPorts method, IVdsLunControllerPorts.AssociateControllerPorts, IVdsLunControllerPorts::AssociateControllerPorts, base.ivdsluncontrollerports_associatecontrollerports, vds/IVdsLunControllerPorts::AssociateControllerPorts, vdshwprv/IVdsLunControllerPorts::AssociateControllerPorts
f1_keywords:
- vdshwprv/IVdsLunControllerPorts.AssociateControllerPorts
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
- IVdsLunControllerPorts.AssociateControllerPorts
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
---

# IVdsLunControllerPorts::AssociateControllerPorts


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets the subsystem controller ports to active or inactive with respect to the LUN. This method 
    replaces <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-associatecontrollers">IVdsLun::AssociateControllers</a>.


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
The association name was successfully set.

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
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_OBJECT_NOT_FOUND</b></b></dt>
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
<dt><b><b>VDS_E_NOT_SUPPORTED</b></b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
This operation or combination of parameters is not supported by this provider.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsluncontrollerports">IVdsLunControllerPorts</a>
 

 

