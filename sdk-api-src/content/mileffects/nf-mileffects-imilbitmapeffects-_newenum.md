---
UID: NF:mileffects.IMILBitmapEffects._NewEnum
title: IMILBitmapEffects::_NewEnum
author: windows-driver-content
description: Retrieves a new enumeration.
old-location: wibe\_wibe_imilbitmapeffects__newenum.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffects\_newenum.htm
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IMILBitmapEffects interface [WPF Bitmap Effects],_NewEnum method, IMILBitmapEffects._NewEnum, IMILBitmapEffects::_NewEnum, _NewEnum, _NewEnum method [WPF Bitmap Effects], _NewEnum method [WPF Bitmap Effects],IMILBitmapEffects interface, _wibe_imilbitmapeffects__newenum, mileffects/IMILBitmapEffects::_NewEnum, wibe._wibe_imilbitmapeffects__newenum
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
-	IMILBitmapEffects._NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffects::_NewEnum


## -description


Retrieves a new enumeration.


## -parameters




### -param ppiuReturn [out, retval]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

A pointer that receives a pointer to the new enumeration item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



