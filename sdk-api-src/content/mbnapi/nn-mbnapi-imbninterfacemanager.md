---
UID: NN:mbnapi.IMbnInterfaceManager
title: IMbnInterfaceManager (mbnapi.h)
author: windows-sdk-content
description: Provides access to IMbnInterface objects and notifications.
old-location: mbn\imbninterfacemanager.htm
tech.root: mbn
ms.assetid: a998381e-47de-4352-bc84-b6edca2f3fcc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMbnInterfaceManager, IMbnInterfaceManager interface [Microsoft Broadband Networks], IMbnInterfaceManager interface [Microsoft Broadband Networks],described, mbn.imbninterfacemanager, mbnapi/IMbnInterfaceManager
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
 - IMbnInterfaceManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnInterfaceManager interface


## -description


Provides access to <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> objects and notifications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnInterfaceManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnInterfaceManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnInterfaceManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f44aa20d-7edd-4227-8eca-9aacb19619e8">GetInterface</a>
</td>
<td align="left" width="63%">
Gets a specific interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1cd10189-8f36-4bcb-95e9-35064e70fdf8">GetInterfaces</a>
</td>
<td align="left" width="63%">
Gets a list of all available interfaces.

</td>
</tr>
</table> 


## -remarks



This interface can be used to access the following notification interfaces.<table>
<tr>
<th>Notification Sink to Register</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/1d421668-cbea-4457-bbc3-dad1b53a5d70">IMbnInterfaceManagerEvents</a>
</td>
<td><b>IID_IMbnInterfaceManagerEvents</b></td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>
</td>
<td><b>IID_IMbnInterfaceEvents</b></td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/9e52168a-c6f9-4154-b8b9-8ae6cb771d46">IMbnSignalEvents</a>
</td>
<td><b>IID_IMbnSignalEvents</b></td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/2942bd4d-5bdb-45eb-a008-352bf44eec80">IMbnPinManagerEvents</a>
</td>
<td><b>IID_IMbnPinManagerEvents</b></td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4bdaa4e5-880e-4d1f-aec1-36811a0f21c1">IMbnPinEvents</a>
</td>
<td><b>IID_IMbnPinEvents</b></td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a>
</td>
<td><b>IID_IMbnRegistrationEvents</b></td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/1f73260b-04db-410a-ade0-a835805b2b0a">IMbnConnectionContextEvents</a>
</td>
<td><b>IID_IMbnConnectionContextEvents</b></td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/06dfb631-fe5a-45d9-89f9-1f13990500ee">IMbnSmsEvents</a>
</td>
<td><b>IID_IMbnSmsEvents</b></td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b3385523-f1ab-403d-9244-7683a7e9f95a">IMbnServiceActivationEvents</a>
</td>
<td><b>IID_IMbnServiceActivationEvents</b></td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/28507e68-5eaa-4b9d-bbb4-e276f4c213d5">IMbnVendorSpecificEvents</a>
</td>
<td><b>IID_IMbnVendorSpecificEvents</b></td>
</tr>
</table>
 



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <b>IMbnInterfaceManager</b> object.</li>
<li>
For each notification sink to register, call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass IID corresponding to the notification sink to <i>riid</i>.

</li>
<li>For each connection point returned by step 2, call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements the matching notification interface to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



