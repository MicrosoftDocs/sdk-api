---
UID: NF:mileffects.IMILBitmapEffectInputConnector.GetConnection
title: IMILBitmapEffectInputConnector::GetConnection (mileffects.h)
description: Gets the IMILBitmapEffectOutputConnector the input connector is connected to.
old-location: wibe\_wibe_imilbitmapeffectinputconnector_getconnection.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectinputconnector\getconnection.htm
ms.date: 12/05/2018
ms.keywords: GetConnection, GetConnection method [WPF Bitmap Effects], GetConnection method [WPF Bitmap Effects],IMILBitmapEffectInputConnector interface, IMILBitmapEffectInputConnector interface [WPF Bitmap Effects],GetConnection method, IMILBitmapEffectInputConnector.GetConnection, IMILBitmapEffectInputConnector::GetConnection, _wibe_imilbitmapeffectinputconnector_getconnection, mileffects/IMILBitmapEffectInputConnector::GetConnection, wibe._wibe_imilbitmapeffectinputconnector_getconnection
ms.topic: method
f1_keywords:
- mileffects/IMILBitmapEffectInputConnector.GetConnection
dev_langs:
- c++
req.header: mileffects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mileffects.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mileffects.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mileffects.dll
api_name:
- IMILBitmapEffectInputConnector.GetConnection
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffectInputConnector::GetConnection


## -description


Gets the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectoutputconnector">IMILBitmapEffectOutputConnector</a> the input connector is connected to.


## -parameters




### -param ppConnector [out, retval]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectoutputconnector">IMILBitmapEffectOutputConnector</a>**</b>

A pointer that receives a pointer to the associated output connector.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



