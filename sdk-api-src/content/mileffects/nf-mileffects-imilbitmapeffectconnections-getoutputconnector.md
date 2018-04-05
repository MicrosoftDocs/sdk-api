---
UID: NF:mileffects.IMILBitmapEffectConnections.GetOutputConnector
title: IMILBitmapEffectConnections::GetOutputConnector method
author: windows-driver-content
description: Retrieves the output connector associated with the given pin index.
old-location: wibe\_wibe_imilbitmapeffectconnections_getoutputconnector.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnections\getoutputconnector.htm
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetOutputConnector method [WPF Bitmap Effects], GetOutputConnector method [WPF Bitmap Effects], IMILBitmapEffectConnections interface, GetOutputConnector,IMILBitmapEffectConnections.GetOutputConnector, IMILBitmapEffectConnections, IMILBitmapEffectConnections interface [WPF Bitmap Effects], GetOutputConnector method, IMILBitmapEffectConnections::GetOutputConnector, _wibe_imilbitmapeffectconnections_getoutputconnector, mileffects/IMILBitmapEffectConnections::GetOutputConnector, wibe._wibe_imilbitmapeffectconnections_getoutputconnector
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
-	IMILBitmapEffectConnections.GetOutputConnector
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectConnections::GetOutputConnector method


## -description


Retrieves the output connector associated with the given pin index.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating which output pin to use to retrieve the output connector.


### -param ppConnector [out, retval]

Type: <b><a href="https://msdn.microsoft.com/36a2d9da-7a25-4316-acdf-8add4016f18f">IMILBitmapEffectOutputConnector</a>**</b>

When this method returns, contains the output connector for the given output pin.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



