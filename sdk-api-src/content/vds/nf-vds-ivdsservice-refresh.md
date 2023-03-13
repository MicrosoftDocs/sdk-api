---
UID: NF:vds.IVdsService.Refresh
title: IVdsService::Refresh (vds.h)
description: Refreshes disk-ownership and disk-layout information.
helpviewer_keywords: ["IVdsService interface [VDS]","Refresh method","IVdsService.Refresh","IVdsService::Refresh","Refresh","Refresh method [VDS]","Refresh method [VDS]","IVdsService interface","base.ivdsservice_refresh","vds/IVdsService::Refresh"]
old-location: base\ivdsservice_refresh.htm
tech.root: base
ms.assetid: ca6a1143-b5f0-49e5-8505-836c565aabcf
ms.date: 12/05/2018
ms.keywords: IVdsService interface [VDS],Refresh method, IVdsService.Refresh, IVdsService::Refresh, Refresh, Refresh method [VDS], Refresh method [VDS],IVdsService interface, base.ivdsservice_refresh, vds/IVdsService::Refresh
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
 - IVdsService::Refresh
 - vds/IVdsService::Refresh
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
 - IVdsService.Refresh
---

# IVdsService::Refresh


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Refreshes disk-ownership and disk-layout information.



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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during this operation.

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
VDS failed to initialize. If an application calls this method before the service finishes initializing, the method is blocked until the initialization completes. If the initialization fails, this error is returned.

</td>
</tr>
</table>

## -remarks

This method synchronizes the disk layout to the layout known to the disk driver. It does not force the driver to read the layout from the disk. Additionally, this method refreshes the view of all objects in the VDS cache. VDS and the providers query all objects, sending object arrival, modification, removal notifications to synchronize the caller. Note that VDS updates the cache automatically whenever it detects a change that triggers a notification. For this reason, and because calling <b>Refresh</b> can trigger additional notifications, applications should not call this method in response to notifications. <b>Refresh</b> should be called only when it appears that the cache is not being updated properly.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsservice">IVdsService</a>
