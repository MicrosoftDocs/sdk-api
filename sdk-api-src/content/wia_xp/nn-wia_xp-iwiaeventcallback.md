---
UID: NN:wia_xp.IWiaEventCallback
title: IWiaEventCallback (wia_xp.h)
author: windows-sdk-content
description: The IWiaEventCallback interface is used by applications to receive notification of Windows Image Acquisition (WIA) hardware device events.
old-location: wia\_wia_IWiaEventCallback.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaeventcallback\iwiaeventcallback.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWiaEventCallback, IWiaEventCallback interface [WIA], IWiaEventCallback interface [WIA],described, _wia_IWiaEventCallback, wia._wia_IWiaEventCallback, wia_xp/IWiaEventCallback
ms.topic: interface
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: Wiaguid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaguid.lib
 - Wiaguid.dll
api_name:
 - IWiaEventCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWiaEventCallback interface


## -description


The <b>IWiaEventCallback</b> interface is used by applications to receive notification of Windows Image Acquisition (WIA) hardware device events. An application registers itself to receive event notifications by passing a pointer to the <b>IWiaEventCallback</b> interface to the <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface">IWiaDevMgr::RegisterEventCallbackInterface</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaEventCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWiaEventCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWiaEventCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback">ImageEventCallback</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback">IWiaEventCallback::ImageEventCallback</a> method is invoked by the WIA run-time system when a hardware device event occurs.

</td>
</tr>
</table> 


## -remarks



The <b>IWiaEventCallback</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods. 

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>
 



