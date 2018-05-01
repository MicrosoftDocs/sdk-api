---
UID: NF:mileffects.IMILBitmapEffectConnector.GetBitmapEffect
title: IMILBitmapEffectConnector::GetBitmapEffect method
author: windows-driver-content
description: Gets the IMILBitmapEffect associated with the connector.
old-location: wibe\_wibe_imilbitmapeffectconnector_getbitmapeffect.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnector\getbitmapeffect.htm
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetBitmapEffect method [WPF Bitmap Effects], GetBitmapEffect method [WPF Bitmap Effects], IMILBitmapEffectConnector interface, GetBitmapEffect,IMILBitmapEffectConnector.GetBitmapEffect, IMILBitmapEffectConnector, IMILBitmapEffectConnector interface [WPF Bitmap Effects], GetBitmapEffect method, IMILBitmapEffectConnector::GetBitmapEffect, _wibe_imilbitmapeffectconnector_getbitmapeffect, mileffects/IMILBitmapEffectConnector::GetBitmapEffect, wibe._wibe_imilbitmapeffectconnector_getbitmapeffect
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
-	IMILBitmapEffectConnector.GetBitmapEffect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectConnector::GetBitmapEffect method


## -description


Gets the <a href="https://msdn.microsoft.com/74078eaa-ae95-4b9b-993b-efbfb18a164d">IMILBitmapEffect</a> associated with the connector.


## -parameters




### -param ppEffect [out, retval]

Type: <b><a href="https://msdn.microsoft.com/74078eaa-ae95-4b9b-993b-efbfb18a164d">IMILBitmapEffect</a>**</b>

A pointer that receives a pointer to the bitmap effect.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



