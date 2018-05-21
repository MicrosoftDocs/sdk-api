---
UID: NF:mileffects.IMILBitmapEffectConnections.GetInputConnector
title: IMILBitmapEffectConnections::GetInputConnector
author: windows-driver-content
description: Retrieves the input connector associated with the given pin index.
old-location: wibe\_wibe_imilbitmapeffectconnections_getinputconnector.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnections\getinputconnector.htm
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: GetInputConnector, GetInputConnector method [WPF Bitmap Effects], GetInputConnector method [WPF Bitmap Effects],IMILBitmapEffectConnections interface, IMILBitmapEffectConnections interface [WPF Bitmap Effects],GetInputConnector method, IMILBitmapEffectConnections.GetInputConnector, IMILBitmapEffectConnections::GetInputConnector, _wibe_imilbitmapeffectconnections_getinputconnector, mileffects/IMILBitmapEffectConnections::GetInputConnector, wibe._wibe_imilbitmapeffectconnections_getinputconnector
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
-	Mileffects.h
api_name:
-	IMILBitmapEffectConnections.GetInputConnector
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectConnections::GetInputConnector


## -description


Retrieves the input connector associated with the given pin index.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating which input pin to use to retrieve the input connector.


### -param ppConnector [out, retval]

Type: <b><a href="https://msdn.microsoft.com/930ffa74-8a38-44c2-8b1c-74c0839d1a5d">IMILBitmapEffectInputConnector</a>**</b>

When this method returns, contains the input connector for the given input pin.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



