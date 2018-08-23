---
UID: NF:mileffects.IMILBitmapEffectGroup.GetInteriorInputConnector
title: IMILBitmapEffectGroup::GetInteriorInputConnector
author: windows-sdk-content
description: Retrieves the input connector for an effect at the given index.
old-location: wibe\_wibe_imilbitmapeffectgroup_getinteriorinputconnector.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectgroup\getinteriorinputconnector.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetInteriorInputConnector, GetInteriorInputConnector method [WPF Bitmap Effects], GetInteriorInputConnector method [WPF Bitmap Effects],IMILBitmapEffectGroup interface, IMILBitmapEffectGroup interface [WPF Bitmap Effects],GetInteriorInputConnector method, IMILBitmapEffectGroup.GetInteriorInputConnector, IMILBitmapEffectGroup::GetInteriorInputConnector, _wibe_imilbitmapeffectgroup_getinteriorinputconnector, mileffects/IMILBitmapEffectGroup::GetInteriorInputConnector, wibe._wibe_imilbitmapeffectgroup_getinteriorinputconnector
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
 - IMILBitmapEffectGroup.GetInteriorInputConnector
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectGroup::GetInteriorInputConnector


## -description


Retrieves the input connector for an effect at the given index.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

The index of the effect to retrieve the connector.


### -param ppConnector [out, retval]

Type: <b><a href="https://msdn.microsoft.com/36a2d9da-7a25-4316-acdf-8add4016f18f">IMILBitmapEffectOutputConnector</a>**</b>

A pointer that receives a pointer to the desired effects input connector.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



