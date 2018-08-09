---
UID: NF:mileffects.IMILBitmapEffectEvents.DirtyRegion
title: IMILBitmapEffectEvents::DirtyRegion
author: windows-sdk-content
description: Invalidates the specified region of the given IMILBitmapEffectPrimitive.
old-location: wibe\_wibe_imilbitmapeffectevents_dirtyregion.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectevents\dirtyregion.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: DirtyRegion, DirtyRegion method [WPF Bitmap Effects], DirtyRegion method [WPF Bitmap Effects],IMILBitmapEffectEvents interface, IMILBitmapEffectEvents interface [WPF Bitmap Effects],DirtyRegion method, IMILBitmapEffectEvents.DirtyRegion, IMILBitmapEffectEvents::DirtyRegion, _wibe_imilbitmapeffectevents_dirtyregion, mileffects/IMILBitmapEffectEvents::DirtyRegion, wibe._wibe_imilbitmapeffectevents_dirtyregion
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
 - IMILBitmapEffectEvents.DirtyRegion
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectEvents::DirtyRegion


## -description


Invalidates the specified region of the given <a href="https://msdn.microsoft.com/23eea785-8545-44d3-bfcb-1ffbc82ecc6a">IMILBitmapEffectPrimitive</a>.


## -parameters




### -param pEffect [in]

Type: <b><a href="https://msdn.microsoft.com/74078eaa-ae95-4b9b-993b-efbfb18a164d">IMILBitmapEffect</a>*</b>

A pointer to the primitive to dirty.


### -param pRect [in]

Type: <b><a href="https://msdn.microsoft.com/da11ec7a-3d36-49b2-be4d-cbc05517d364">MIL_RECTD</a>*</b>

A pointer to the rectangle to dirty.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



