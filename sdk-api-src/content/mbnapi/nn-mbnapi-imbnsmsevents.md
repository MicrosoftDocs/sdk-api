---
UID: NN:mbnapi.IMbnSmsEvents
title: IMbnSmsEvents
author: windows-sdk-content
description: This notification interface signals an application with the completion status of SMS operations and changes in the device SMS status.
old-location: mbn\imbnsmsevents.htm
old-project: mbn
ms.assetid: 06dfb631-fe5a-45d9-89f9-1f13990500ee
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IMbnSmsEvents, IMbnSmsEvents interface [Microsoft Broadband Networks], IMbnSmsEvents interface [Microsoft Broadband Networks],described, mbn.imbnsmsevents, mbnapi/IMbnSmsEvents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnSmsEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnSmsEvents interface


## -description


This notification interface signals an application with the completion status of SMS operations and changes in the device SMS status.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnSmsEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnSmsEvents</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d5e5b1fc-88c3-4438-a160-f9969ed6d91a">OnSetSmsConfigurationComplete</a>
</td>
<td align="left" width="63%">
A set SMS configuration operation has completed, or the SMS subsystem is initialized and ready for operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6990732-60ef-43e5-b35c-9a3f0324d580">OnSmsConfigurationChange</a>
</td>
<td align="left" width="63%">
The SMS configuration is available or changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bac1c7b3-fedc-47fb-822c-712805a86f6e">OnSmsDeleteComplete</a>
</td>
<td align="left" width="63%">
A SMS delete operation has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6d13393-557c-462c-a640-2228ab0c9c17">OnSmsNewClass0Message</a>
</td>
<td align="left" width="63%">
A new Class0/Flash message was received by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58478c9d-6df2-466b-85bc-1c571f4429ce">OnSmsReadComplete</a>
</td>
<td align="left" width="63%">
A SMS read operation has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c08b173-7e9e-4b4f-8068-1a90c57eea90">OnSmsSendComplete</a>
</td>
<td align="left" width="63%">
A SMS send operation has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a3027e2-f8ee-476a-96e2-29ef4d87db38">OnSmsStatusChange</a>
</td>
<td align="left" width="63%">
The has been a change in the status of the device message store.

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="https://msdn.microsoft.com/a998381e-47de-4352-bc84-b6edca2f3fcc">IMbnInterfaceManager</a> object.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnSmsEvents</b> to <i>riid</i>.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnSmsEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



