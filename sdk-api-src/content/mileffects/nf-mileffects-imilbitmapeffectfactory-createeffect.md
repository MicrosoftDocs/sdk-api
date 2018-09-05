---
UID: NF:mileffects.IMILBitmapEffectFactory.CreateEffect
title: IMILBitmapEffectFactory::CreateEffect
author: windows-sdk-content
description: Creates an IMILBitmapEffect object.
old-location: wibe\_wibe_imilbitmapeffectfactory_createeffect.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectfactory\createeffect.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateEffect, CreateEffect method [WPF Bitmap Effects], CreateEffect method [WPF Bitmap Effects],IMILBitmapEffectFactory interface, IMILBitmapEffectFactory interface [WPF Bitmap Effects],CreateEffect method, IMILBitmapEffectFactory.CreateEffect, IMILBitmapEffectFactory::CreateEffect, _wibe_imilbitmapeffectfactory_createeffect, mileffects/IMILBitmapEffectFactory::CreateEffect, wibe._wibe_imilbitmapeffectfactory_createeffect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mileffects.h
req.include-header: 
req.redist: Microsoft .Net 3.0
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
tech.root: 
req.typenames: MICUIELEMENTSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.dll
api_name:
 - IMILBitmapEffectFactory.CreateEffect
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectFactory::CreateEffect


## -description


Creates an <a href="https://msdn.microsoft.com/74078eaa-ae95-4b9b-993b-efbfb18a164d">IMILBitmapEffect</a> object.


## -parameters




### -param pguidEffect [in]

Type: <b>const GUID*</b>

A pointer to the GUID of the effect to create.


### -param ppEffect [out]

Type: <b><a href="https://msdn.microsoft.com/74078eaa-ae95-4b9b-993b-efbfb18a164d">IMILBitmapEffect</a>**</b>

A pointer that receives a pointer to a new <a href="https://msdn.microsoft.com/23eea785-8545-44d3-bfcb-1ffbc82ecc6a">IMILBitmapEffectPrimitive</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



