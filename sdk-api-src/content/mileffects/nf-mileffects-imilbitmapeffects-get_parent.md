---
UID: NF:mileffects.IMILBitmapEffects.get_Parent
title: IMILBitmapEffects::get_Parent
author: windows-sdk-content
description: Retrieves the parent effect group of enumeration.
old-location: wibe\_wibe_imilbitmapeffects_parent.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffects\parent.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMILBitmapEffects interface [WPF Bitmap Effects],get_Parent method, IMILBitmapEffects.get_Parent, IMILBitmapEffects::get_Parent, _wibe_imilbitmapeffects_parent, get_Parent, get_Parent method [WPF Bitmap Effects], get_Parent method [WPF Bitmap Effects],IMILBitmapEffects interface, mileffects/IMILBitmapEffects::get_Parent, wibe._wibe_imilbitmapeffects_parent
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.h
api_name:
 - IMILBitmapEffects.get_Parent
product: Windows
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
---

# IMILBitmapEffects::get_Parent


## -description


Retrieves the parent effect group of enumeration.


## -parameters




### -param ppEffect [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms735291(v=VS.85).aspx">IMILBitmapEffectGroup</a>**</b>

A pointer that receives a pointer to the parent group.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



