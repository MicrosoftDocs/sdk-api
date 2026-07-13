---
UID: NN:wia_xp.IWiaDevMgr
title: IWiaDevMgr (wia_xp.h)
description: Applications use the IWiaDevMgr interface to create and manage image acquisition devices.
helpviewer_keywords: ["IWiaDevMgr","IWiaDevMgr interface [WIA]","IWiaDevMgr interface [WIA]","described","_wia_IWiaDevMgr","wia._wia_IWiaDevMgr","wia_xp/IWiaDevMgr"]
old-location: wia\_wia_IWiaDevMgr.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadevmgr\iwiadevmgr.htm
ms.date: 12/05/2018
ms.keywords: IWiaDevMgr, IWiaDevMgr interface [WIA], IWiaDevMgr interface [WIA],described, _wia_IWiaDevMgr, wia._wia_IWiaDevMgr, wia_xp/IWiaDevMgr
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
req.dll: Wiaservc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWiaDevMgr
 - wia_xp/IWiaDevMgr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaDevMgr
archived: true
---

# IWiaDevMgr interface


## -description

Applications use the <b>IWiaDevMgr</b> interface to create and manage image acquisition devices. They also use it to register to receive device events.
<div class="alert"><b>Note</b>  For Windows Vista applications, use <a href="/windows/desktop/wia/-wia-iwiadevmgr2">IWiaDevMgr2</a> instead of <b>IWiaDevMgr</b>.</div><div> </div>

## -inheritance

The <b>IWiaDevMgr</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWiaDevMgr</b> also has these types of members:

## -remarks

The <b>IWiaDevMgr</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods. 

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
