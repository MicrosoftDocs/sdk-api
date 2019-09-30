---
UID: NN:mbnapi.IMbnSmsEvents
title: IMbnSmsEvents (mbnapi.h)
author: windows-sdk-content
description: This notification interface signals an application with the completion status of SMS operations and changes in the device SMS status.
old-location: mbn\imbnsmsevents.htm
tech.root: mbn
ms.assetid: 06dfb631-fe5a-45d9-89f9-1f13990500ee
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnSmsEvents, IMbnSmsEvents interface [Microsoft Broadband Networks], IMbnSmsEvents interface [Microsoft Broadband Networks],described, mbn.imbnsmsevents, mbnapi/IMbnSmsEvents
ms.topic: interface
f1_keywords: 
 - "mbnapi/IMbnSmsEvents"
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - mbnapi.h
api_name:
 - IMbnSmsEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnSmsEvents interface


## -description


This notification interface signals an application with the completion status of SMS operations and changes in the device SMS status.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnSmsEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnSmsEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnSmsEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsetsmsconfigurationcomplete">OnSetSmsConfigurationComplete</a>
</td>
<td align="left" width="63%">
A set SMS configuration operation has completed, or the SMS subsystem is initialized and ready for operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmsconfigurationchange">OnSmsConfigurationChange</a>
</td>
<td align="left" width="63%">
The SMS configuration is available or changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmsdeletecomplete">OnSmsDeleteComplete</a>
</td>
<td align="left" width="63%">
A SMS delete operation has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmsnewclass0message">OnSmsNewClass0Message</a>
</td>
<td align="left" width="63%">
A new Class0/Flash message was received by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmsreadcomplete">OnSmsReadComplete</a>
</td>
<td align="left" width="63%">
A SMS read operation has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmssendcomplete">OnSmsSendComplete</a>
</td>
<td align="left" width="63%">
A SMS send operation has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmsstatuschange">OnSmsStatusChange</a>
</td>
<td align="left" width="63%">
The has been a change in the status of the device message store.

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager">IMbnInterfaceManager</a> object.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnSmsEvents</b> to <i>riid</i>.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnSmsEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



