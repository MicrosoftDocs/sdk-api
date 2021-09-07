---
UID: NF:mileffects.IMILBitmapEffectInputConnector.ConnectTo
title: IMILBitmapEffectInputConnector::ConnectTo (mileffects.h)
description: Connects the input connector to the given output connector.
helpviewer_keywords: ["ConnectTo","ConnectTo method [WPF Bitmap Effects]","ConnectTo method [WPF Bitmap Effects]","IMILBitmapEffectInputConnector interface","IMILBitmapEffectInputConnector interface [WPF Bitmap Effects]","ConnectTo method","IMILBitmapEffectInputConnector.ConnectTo","IMILBitmapEffectInputConnector::ConnectTo","_wibe_imilbitmapeffectinputconnector_connectto","mileffects/IMILBitmapEffectInputConnector::ConnectTo","wibe._wibe_imilbitmapeffectinputconnector_connectto"]
old-location: wibe\_wibe_imilbitmapeffectinputconnector_connectto.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectinputconnector\connectto.htm
ms.date: 12/05/2018
ms.keywords: ConnectTo, ConnectTo method [WPF Bitmap Effects], ConnectTo method [WPF Bitmap Effects],IMILBitmapEffectInputConnector interface, IMILBitmapEffectInputConnector interface [WPF Bitmap Effects],ConnectTo method, IMILBitmapEffectInputConnector.ConnectTo, IMILBitmapEffectInputConnector::ConnectTo, _wibe_imilbitmapeffectinputconnector_connectto, mileffects/IMILBitmapEffectInputConnector::ConnectTo, wibe._wibe_imilbitmapeffectinputconnector_connectto
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
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
f1_keywords:
 - IMILBitmapEffectInputConnector::ConnectTo
 - mileffects/IMILBitmapEffectInputConnector::ConnectTo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.dll
api_name:
 - IMILBitmapEffectInputConnector.ConnectTo
---

# IMILBitmapEffectInputConnector::ConnectTo


## -description

Connects the input connector to the given output connector.

## -parameters

### -param pConnector [in]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectoutputconnector">IMILBitmapEffectOutputConnector</a>*</b>

A pointer to the connector to connect the input to.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.