---
UID: NN:wsbapp.IWsbApplicationAsync
title: IWsbApplicationAsync (wsbapp.h)

description: Defines methods to monitor and control the progress of an asynchronous operation.
old-location: wsb\iwsbapplicationasync.htm
tech.root: wsb
ms.assetid: cd8f74c0-c2dc-487c-b702-1e1355e99b7d

ms.date: 12/05/2018
ms.keywords: IWsbApplicationAsync, IWsbApplicationAsync interface [Windows Server Backup], IWsbApplicationAsync interface [Windows Server Backup],described, wsb.iwsbapplicationasync, wsbapp/IWsbApplicationAsync
ms.topic: interface
f1_keywords: 
 - "wsbapp/IWsbApplicationAsync"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWsbApplicationAsync interface


## -description


Defines methods to monitor and control the progress of an asynchronous operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWsbApplicationAsync</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWsbApplicationAsync</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wsbapp/nf-wsbapp-iwsbapplicationasync-abort">Abort</a>
</td>
<td align="left" width="63%">
Cancels an incomplete asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wsbapp/nf-wsbapp-iwsbapplicationasync-querystatus">QueryStatus</a>
</td>
<td align="left" width="63%">
Queries the status of an asynchronous operation.

</td>
</tr>
</table> 

