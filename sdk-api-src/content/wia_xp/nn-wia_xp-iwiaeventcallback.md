---
UID: NN:wia_xp.IWiaEventCallback
title: IWiaEventCallback (wia_xp.h)
description: The IWiaEventCallback interface is used by applications to receive notification of Windows Image Acquisition (WIA) hardware device events.
helpviewer_keywords: ["IWiaEventCallback","IWiaEventCallback interface [WIA]","IWiaEventCallback interface [WIA]","described","_wia_IWiaEventCallback","wia._wia_IWiaEventCallback","wia_xp/IWiaEventCallback"]
old-location: wia\_wia_IWiaEventCallback.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaeventcallback\iwiaeventcallback.htm
ms.date: 12/05/2018
ms.keywords: IWiaEventCallback, IWiaEventCallback interface [WIA], IWiaEventCallback interface [WIA],described, _wia_IWiaEventCallback, wia._wia_IWiaEventCallback, wia_xp/IWiaEventCallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWiaEventCallback
 - wia_xp/IWiaEventCallback
dev_langs:
 - c++
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
archived: true
---

# IWiaEventCallback interface


## -description

The <b>IWiaEventCallback</b> interface is used by applications to receive notification of Windows Image Acquisition (WIA) hardware device events. An application registers itself to receive event notifications by passing a pointer to the <b>IWiaEventCallback</b> interface to the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface">IWiaDevMgr::RegisterEventCallbackInterface</a> method.

## -inheritance

The <b>IWiaEventCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWiaEventCallback</b> also has these types of members:

## -remarks

The <b>IWiaEventCallback</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods. 

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>
