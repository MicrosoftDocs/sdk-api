---
UID: NF:vdshwprv.IVdsAdviseSink.OnNotify
title: IVdsAdviseSink::OnNotify (vdshwprv.h)
description: The IVdsAdviseSink::OnNotify method (vdshwprv.h) passes notifications from providers to VDS, and from VDS to applications. 
helpviewer_keywords: ["IVdsAdviseSink interface [VDS]","OnNotify method","IVdsAdviseSink.OnNotify","IVdsAdviseSink::OnNotify","OnNotify","OnNotify method [VDS]","OnNotify method [VDS]","IVdsAdviseSink interface","base.ivdsadvisesink_onnotify","vds/IVdsAdviseSink::OnNotify","vdshwprv/IVdsAdviseSink::OnNotify"]
old-location: base\ivdsadvisesink_onnotify.htm
tech.root: base
ms.assetid: 0cf7bf55-922e-4092-bb2f-6423d9addb0c
ms.date: 08/08/2022
ms.keywords: IVdsAdviseSink interface [VDS],OnNotify method, IVdsAdviseSink.OnNotify, IVdsAdviseSink::OnNotify, OnNotify, OnNotify method [VDS], OnNotify method [VDS],IVdsAdviseSink interface, base.ivdsadvisesink_onnotify, vds/IVdsAdviseSink::OnNotify, vdshwprv/IVdsAdviseSink::OnNotify
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
 - IVdsAdviseSink::OnNotify
 - vdshwprv/IVdsAdviseSink::OnNotify
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
 - IVdsAdviseSink.OnNotify
---

# IVdsAdviseSink::OnNotify


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Passes notifications 
   from providers to VDS, and from VDS to applications.

## -parameters

### -param lNumberOfNotifications [in]

The number of notifications specified in <i>pNotificationArray</i>.

### -param pNotificationArray [in]

A pointer to an array of <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> 
      structures. A provider allocates the memory for the array when the provider calls into the service; the 
      service frees the array. VDS allocates the array when the service calls into an application. In this case, 
      callers must free the array by using the 
      <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
VDS returns this value to a provider if the service is not fully initialized when the provider calls into 
        this method, or if some notifications are lost by the service.

</td>
</tr>
</table>

## -remarks

An application implements this method to receive notifications from VDS. Some of these notifications originate from VDS; others are provider notifications that are forwarded by VDS.

VDS maintains a cache of information about the properties of all VDS objects, such as subsystems and controllers. Whenever a change occurs that triggers a notification, this cache is updated automatically. Also, calling <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> or <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-refresh">IVdsService::Refresh</a> in response to a VDS notification could cause an endless loop of notifications to be sent. For these reasons, an application should not call <b>IVdsHwProvider::Refresh</b> or <b>IVdsService::Refresh</b> in its implementation of this method. 

For providers that use this method to send notifications, it is good practice to group notifications originating from a single event together. For example, when a LUN 
    is deleted, send <b>VDS_NF_DRIVE_MODIFY</b> notifications for all affected drives 
    together.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-refresh">IVdsService::Refresh</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-unadvise">IVdsService::Unadvise</a>



<a href="/windows/desktop/VDS/vds-notification-model">VDS Notifications</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>
