---
UID: NF:mileffects.IMILBitmapEffectEvents.PropertyChange
title: IMILBitmapEffectEvents::PropertyChange
author: windows-sdk-content
description: Notifies an IMILBitmapEffectPrimitive of a property change.
old-location: wibe\_wibe_imilbitmapeffectevents_propertychange.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectevents\propertychange.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: IMILBitmapEffectEvents interface [WPF Bitmap Effects],PropertyChange method, IMILBitmapEffectEvents.PropertyChange, IMILBitmapEffectEvents::PropertyChange, PropertyChange, PropertyChange method [WPF Bitmap Effects], PropertyChange method [WPF Bitmap Effects],IMILBitmapEffectEvents interface, _wibe_imilbitmapeffectevents_propertychange, mileffects/IMILBitmapEffectEvents::PropertyChange, wibe._wibe_imilbitmapeffectevents_propertychange
ms.prod: windows
ms.technology: windows-sdk
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
 - IMILBitmapEffectEvents.PropertyChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectEvents::PropertyChange


## -description


Notifies an <a href="https://msdn.microsoft.com/library/ms735258(v=VS.85).aspx">IMILBitmapEffectPrimitive</a> of a property change.


## -parameters




### -param pEffect [in]

Type: <b><a href="https://msdn.microsoft.com/library/ms735317(v=VS.85).aspx">IMILBitmapEffect</a>*</b>

The effect primitive to notify.


### -param bstrPropertyName [in]

Type: <b>BSTR</b>

The property that has changed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



