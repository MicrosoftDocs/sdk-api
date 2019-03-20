---
UID: NN:wsbapp.IWsbApplicationAsync
title: IWsbApplicationAsync (wsbapp.h)
author: windows-sdk-content
description: Defines methods to monitor and control the progress of an asynchronous operation.
old-location: wsb\iwsbapplicationasync.htm
tech.root: wsb
ms.assetid: cd8f74c0-c2dc-487c-b702-1e1355e99b7d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWsbApplicationAsync, IWsbApplicationAsync interface [Windows Server Backup], IWsbApplicationAsync interface [Windows Server Backup],described, wsb.iwsbapplicationasync, wsbapp/IWsbApplicationAsync
ms.topic: interface
req.header: wsbapp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsbApp.idl
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
 - WsbApp.h
api_name:
 - IWsbApplicationAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWsbApplicationAsync interface


## -description


Defines methods to monitor and control the progress of an asynchronous operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWsbApplicationAsync</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWsbApplicationAsync</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWsbApplicationAsync</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/937ca809-4bb0-408e-9c7e-eccc43d8d4ae">Abort</a>
</td>
<td align="left" width="63%">
Cancels an incomplete asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0705e4a8-b65e-4740-b073-7fb24e5d02ef">QueryStatus</a>
</td>
<td align="left" width="63%">
Queries the status of an asynchronous operation.

</td>
</tr>
</table> 

