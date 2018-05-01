---
UID: NF:mileffects.IMILBitmapEffectInputConnector.ConnectTo
title: IMILBitmapEffectInputConnector::ConnectTo method
author: windows-driver-content
description: Connects the input connector to the given output connector.
old-location: wibe\_wibe_imilbitmapeffectinputconnector_connectto.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectinputconnector\connectto.htm
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: ConnectTo method [WPF Bitmap Effects], ConnectTo method [WPF Bitmap Effects], IMILBitmapEffectInputConnector interface, ConnectTo,IMILBitmapEffectInputConnector.ConnectTo, IMILBitmapEffectInputConnector, IMILBitmapEffectInputConnector interface [WPF Bitmap Effects], ConnectTo method, IMILBitmapEffectInputConnector::ConnectTo, _wibe_imilbitmapeffectinputconnector_connectto, mileffects/IMILBitmapEffectInputConnector::ConnectTo, wibe._wibe_imilbitmapeffectinputconnector_connectto
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mileffects.dll
api_name:
-	IMILBitmapEffectInputConnector.ConnectTo
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectInputConnector::ConnectTo method


## -description


Connects the input connector to the given output connector.


## -parameters




### -param pConnector [in]

Type: <b><a href="https://msdn.microsoft.com/36a2d9da-7a25-4316-acdf-8add4016f18f">IMILBitmapEffectOutputConnector</a>*</b>

A pointer to the connector to connect the input to.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



