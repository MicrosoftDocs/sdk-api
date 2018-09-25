---
UID: NF:mileffects.IMILBitmapEffectFactory.CreateContext
title: IMILBitmapEffectFactory::CreateContext
author: windows-sdk-content
description: Creates an IMILBitmapEffectRenderContext object.
old-location: wibe\_wibe_imilbitmapeffectfactory_createcontext.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectfactory\createcontext.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateContext, CreateContext method [WPF Bitmap Effects], CreateContext method [WPF Bitmap Effects],IMILBitmapEffectFactory interface, IMILBitmapEffectFactory interface [WPF Bitmap Effects],CreateContext method, IMILBitmapEffectFactory.CreateContext, IMILBitmapEffectFactory::CreateContext, _wibe_imilbitmapeffectfactory_createcontext, mileffects/IMILBitmapEffectFactory::CreateContext, wibe._wibe_imilbitmapeffectfactory_createcontext
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
 - IMILBitmapEffectFactory.CreateContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
---

# IMILBitmapEffectFactory::CreateContext


## -description


Creates an <a href="https://msdn.microsoft.com/0c8fbbba-32e6-459c-90ab-2453b57c27ee">IMILBitmapEffectRenderContext</a> object.


## -parameters




### -param ppContext [out]

Type: <b><a href="https://msdn.microsoft.com/0c8fbbba-32e6-459c-90ab-2453b57c27ee">IMILBitmapEffectRenderContext</a>**</b>

A pointer that receives a pointer to a new <a href="https://msdn.microsoft.com/0c8fbbba-32e6-459c-90ab-2453b57c27ee">IMILBitmapEffectRenderContext</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



