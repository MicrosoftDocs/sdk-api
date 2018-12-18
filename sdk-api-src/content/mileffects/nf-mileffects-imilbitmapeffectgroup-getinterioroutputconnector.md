---
UID: NF:mileffects.IMILBitmapEffectGroup.GetInteriorOutputConnector
title: IMILBitmapEffectGroup::GetInteriorOutputConnector
author: windows-sdk-content
description: Retrieves the output connector for an effect at the given index.
old-location: wibe\_wibe_imilbitmapeffectgroup_getinterioroutputconnector.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectgroup\getinterioroutputconnector.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetInteriorOutputConnector, GetInteriorOutputConnector method [WPF Bitmap Effects], GetInteriorOutputConnector method [WPF Bitmap Effects],IMILBitmapEffectGroup interface, IMILBitmapEffectGroup interface [WPF Bitmap Effects],GetInteriorOutputConnector method, IMILBitmapEffectGroup.GetInteriorOutputConnector, IMILBitmapEffectGroup::GetInteriorOutputConnector, _wibe_imilbitmapeffectgroup_getinterioroutputconnector, mileffects/IMILBitmapEffectGroup::GetInteriorOutputConnector, wibe._wibe_imilbitmapeffectgroup_getinterioroutputconnector
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
 - IMILBitmapEffectGroup.GetInteriorOutputConnector
product: Windows
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
---

# IMILBitmapEffectGroup::GetInteriorOutputConnector


## -description


Retrieves the output connector for an effect at the given index.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

The index of the effect to retrieve the connector.


### -param ppConnector [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms735274(v=VS.85).aspx">IMILBitmapEffectInputConnector</a>**</b>

A pointer that receives a pointer to the desired effects output connector.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



