---
UID: NN:wia_xp.IWiaDataCallback
title: IWiaDataCallback (wia_xp.h)
description: Provides an application callback mechanism during data transfers from Windows Image Acquisition (WIA) hardware devices to applications.Note  For Windows Vista applications, use IWiaTransferCallback instead of IWiaDataCallback.
helpviewer_keywords: ["IWiaDataCallback","IWiaDataCallback interface [WIA]","IWiaDataCallback interface [WIA]","described","_wia_IWiaDataCallback","wia._wia_IWiaDataCallback","wia_xp/IWiaDataCallback"]
old-location: wia\_wia_IWiaDataCallback.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadatacallback\iwiadatacallback.htm
ms.date: 12/05/2018
ms.keywords: IWiaDataCallback, IWiaDataCallback interface [WIA], IWiaDataCallback interface [WIA],described, _wia_IWiaDataCallback, wia._wia_IWiaDataCallback, wia_xp/IWiaDataCallback
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
 - IWiaDataCallback
 - wia_xp/IWiaDataCallback
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
 - IWiaDataCallback
archived: true
---

# IWiaDataCallback interface


## -description

Provides an application callback mechanism during data transfers from Windows Image Acquisition (WIA) hardware devices to applications.
<div class="alert"><b>Note</b>  For Windows Vista applications, use <a href="/windows/desktop/wia/-wia-iwiatransfercallback">IWiaTransferCallback</a> instead of <b>IWiaDataCallback</b>.</div><div> </div>

## -inheritance

The <b>IWiaDataCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWiaDataCallback</b> also has these types of members:

## -remarks

The <b>IWiaDataCallback</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods. 

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
