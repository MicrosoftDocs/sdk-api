---
UID: NF:mileffects.IMILBitmapEffects.Item
title: IMILBitmapEffects::Item
author: windows-sdk-content
description: Retrieves the effect at the given index.
old-location: wibe\_wibe_imilbitmapeffects_item.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffects\item.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMILBitmapEffects interface [WPF Bitmap Effects],Item method, IMILBitmapEffects.Item, IMILBitmapEffects::Item, Item, Item method [WPF Bitmap Effects], Item method [WPF Bitmap Effects],IMILBitmapEffects interface, _wibe_imilbitmapeffects_item, mileffects/IMILBitmapEffects::Item, wibe._wibe_imilbitmapeffects_item
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
 - Mileffects.h
api_name:
 - IMILBitmapEffects.Item
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffects::Item


## -description


Retrieves the effect at the given index.


## -parameters




### -param uindex

Type: <b>ULONG</b>

The index of the effect.


### -param ppEffect [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms735317(v=VS.85).aspx">IMILBitmapEffect</a>**</b>

A pointer that receives a pointer to the bitmap effect.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



