---
UID: NF:mileffects.IMILBitmapEffectGroup.GetInteriorOutputConnector
title: IMILBitmapEffectGroup::GetInteriorOutputConnector
author: windows-sdk-content
description: Retrieves the output connector for an effect at the given index.
old-location: wibe\_wibe_imilbitmapeffectgroup_getinterioroutputconnector.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectgroup\getinterioroutputconnector.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetInteriorOutputConnector, GetInteriorOutputConnector method [WPF Bitmap Effects], GetInteriorOutputConnector method [WPF Bitmap Effects],IMILBitmapEffectGroup interface, IMILBitmapEffectGroup interface [WPF Bitmap Effects],GetInteriorOutputConnector method, IMILBitmapEffectGroup.GetInteriorOutputConnector, IMILBitmapEffectGroup::GetInteriorOutputConnector, _wibe_imilbitmapeffectgroup_getinterioroutputconnector, mileffects/IMILBitmapEffectGroup::GetInteriorOutputConnector, wibe._wibe_imilbitmapeffectgroup_getinterioroutputconnector
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
 - Mileffects.h
api_name:
 - IMILBitmapEffectGroup.GetInteriorOutputConnector
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectGroup::GetInteriorOutputConnector


## -description


Retrieves the output connector for an effect at the given index.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

The index of the effect to retrieve the connector.


### -param ppConnector [out, retval]

Type: <b><a href="https://msdn.microsoft.com/930ffa74-8a38-44c2-8b1c-74c0839d1a5d">IMILBitmapEffectInputConnector</a>**</b>

A pointer that receives a pointer to the desired effects output connector.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



