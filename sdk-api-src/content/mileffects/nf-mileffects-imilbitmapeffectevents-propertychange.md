---
UID: NF:mileffects.IMILBitmapEffectEvents.PropertyChange
title: IMILBitmapEffectEvents::PropertyChange
author: windows-sdk-content
description: Notifies an IMILBitmapEffectPrimitive of a property change.
old-location: wibe\_wibe_imilbitmapeffectevents_propertychange.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectevents\propertychange.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMILBitmapEffectEvents interface [WPF Bitmap Effects],PropertyChange method, IMILBitmapEffectEvents.PropertyChange, IMILBitmapEffectEvents::PropertyChange, PropertyChange, PropertyChange method [WPF Bitmap Effects], PropertyChange method [WPF Bitmap Effects],IMILBitmapEffectEvents interface, _wibe_imilbitmapeffectevents_propertychange, mileffects/IMILBitmapEffectEvents::PropertyChange, wibe._wibe_imilbitmapeffectevents_propertychange
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
 - IMILBitmapEffectEvents.PropertyChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
---

# IMILBitmapEffectEvents::PropertyChange


## -description


Notifies an <a href="https://msdn.microsoft.com/23eea785-8545-44d3-bfcb-1ffbc82ecc6a">IMILBitmapEffectPrimitive</a> of a property change.


## -parameters




### -param pEffect [in]

Type: <b><a href="https://msdn.microsoft.com/74078eaa-ae95-4b9b-993b-efbfb18a164d">IMILBitmapEffect</a>*</b>

The effect primitive to notify.


### -param bstrPropertyName [in]

Type: <b>BSTR</b>

The property that has changed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



