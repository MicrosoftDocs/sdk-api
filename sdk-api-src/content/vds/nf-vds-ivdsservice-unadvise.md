---
UID: NF:vds.IVdsService.Unadvise
title: IVdsService::Unadvise (vds.h)
description: Unregisters the caller's IVdsAdviseSink interface so that the caller no longer receives notifications from the VDS service.
helpviewer_keywords: ["IVdsService interface [VDS]","Unadvise method","IVdsService.Unadvise","IVdsService::Unadvise","Unadvise","Unadvise method [VDS]","Unadvise method [VDS]","IVdsService interface","base.ivdsservice_unadvise","vds/IVdsService::Unadvise"]
old-location: base\ivdsservice_unadvise.htm
tech.root: base
ms.assetid: 085d380c-2e09-470a-a23d-704c31535975
ms.date: 12/05/2018
ms.keywords: IVdsService interface [VDS],Unadvise method, IVdsService.Unadvise, IVdsService::Unadvise, Unadvise, Unadvise method [VDS], Unadvise method [VDS],IVdsService interface, base.ivdsservice_unadvise, vds/IVdsService::Unadvise
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
 - IVdsService::Unadvise
 - vds/IVdsService::Unadvise
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
 - IVdsService.Unadvise
---

# IVdsService::Unadvise


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Unregisters the caller's  <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface so that the caller no longer receives notifications from the VDS service.

## -parameters

### -param dwCookie [in]

The cookie that was returned by the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> method when the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface was registered.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_BAD_COOKIE</b></dt>
<dt>0x80042411L</dt>
</dl>
</td>
<td width="60%">
The cookie does not exist.

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

Use the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">Advise</a> method to register your VDS application's  <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface to receive notifications from VDS.  <b>Advise</b> returns a cookie, which you must pass back as a parameter to the <b>Unadvise</b> method.

<div class="alert"><b>Note</b>  An application that calls <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">Advise</a> must eventually call <b>Unadvise</b>. Ideally, it should call <b>Unadvise</b> as soon as it no longer needs to receive notifications.</div>
<div> </div>
The <b>Unadvise</b> method might not return immediately, because it waits for a lock to update the list of registered client applications and waits for the notification thread sending the client notifications to exit. If there are outstanding notifications to be sent to your application, the notification thread tries to send them before exiting.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsservice">IVdsService</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="/windows/desktop/VDS/vds-notification-model">VDS Notifications</a>