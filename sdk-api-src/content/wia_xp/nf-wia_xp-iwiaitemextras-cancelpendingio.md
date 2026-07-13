---
UID: NF:wia_xp.IWiaItemExtras.CancelPendingIO
title: IWiaItemExtras::CancelPendingIO (wia_xp.h)
description: The IWiaItemExtras::CancelPendingIO method cancels all pending input/output operations on the driver.
helpviewer_keywords: ["CancelPendingIO","CancelPendingIO method [WIA]","CancelPendingIO method [WIA]","IWiaItemExtras interface","IWiaItemExtras interface [WIA]","CancelPendingIO method","IWiaItemExtras.CancelPendingIO","IWiaItemExtras::CancelPendingIO","_wia_IWiaItemExtras_CancelPendingIO","wia._wia_IWiaItemExtras_CancelPendingIO","wia_xp/IWiaItemExtras::CancelPendingIO"]
old-location: wia\_wia_IWiaItemExtras_CancelPendingIO.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitemextras\cancelpendingio.htm
ms.date: 12/05/2018
ms.keywords: CancelPendingIO, CancelPendingIO method [WIA], CancelPendingIO method [WIA],IWiaItemExtras interface, IWiaItemExtras interface [WIA],CancelPendingIO method, IWiaItemExtras.CancelPendingIO, IWiaItemExtras::CancelPendingIO, _wia_IWiaItemExtras_CancelPendingIO, wia._wia_IWiaItemExtras_CancelPendingIO, wia_xp/IWiaItemExtras::CancelPendingIO
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
 - IWiaItemExtras::CancelPendingIO
 - wia_xp/IWiaItemExtras::CancelPendingIO
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
 - IWiaItemExtras.CancelPendingIO
archived: true
---

# IWiaItemExtras::CancelPendingIO


## -description

The <b>IWiaItemExtras::CancelPendingIO</b> method cancels all pending input/output operations on the driver.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Drivers are not required to support this method.

