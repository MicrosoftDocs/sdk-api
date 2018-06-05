---
UID: NF:mileffects.IMILBitmapEffectGroup.Add
title: IMILBitmapEffectGroup::Add
author: windows-sdk-content
description: Adds an effect to the IMILBitmapEffectGroup.
old-location: wibe\_wibe_imilbitmapeffectgroup_add.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectgroup\add.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: Add, Add method [WPF Bitmap Effects], Add method [WPF Bitmap Effects],IMILBitmapEffectGroup interface, IMILBitmapEffectGroup interface [WPF Bitmap Effects],Add method, IMILBitmapEffectGroup.Add, IMILBitmapEffectGroup::Add, _wibe_imilbitmapeffectgroup_add, mileffects/IMILBitmapEffectGroup::Add, wibe._wibe_imilbitmapeffectgroup_add
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mileffects.h
api_name:
-	IMILBitmapEffectGroup.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectGroup::Add


## -description


Adds an effect to the <a href="https://msdn.microsoft.com/a8ca1b39-f1b9-40b5-bcec-bf2e3182b9aa">IMILBitmapEffectGroup</a>.


## -parameters




### -param pEffect [in]

Type: <b><a href="https://msdn.microsoft.com/74078eaa-ae95-4b9b-993b-efbfb18a164d">IMILBitmapEffect</a>*</b>

A pointer to the effect to add to the group.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



