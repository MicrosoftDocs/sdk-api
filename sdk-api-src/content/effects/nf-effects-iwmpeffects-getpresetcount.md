---
UID: NF:effects.IWMPEffects.GetPresetCount
title: IWMPEffects::GetPresetCount
author: windows-sdk-content
description: The GetPresetCount method gets the preset count.
old-location: wmp\iwmpeffects_getpresetcount.htm
old-project: WMP
ms.assetid: 6eee859b-8f39-4951-814a-41913df152db
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: EffectsGetPresetCount, GetPresetCount, GetPresetCount method [Windows Media Player], GetPresetCount method [Windows Media Player],IWMPEffects interface, IWMPEffects interface [Windows Media Player],GetPresetCount method, IWMPEffects.GetPresetCount, IWMPEffects::GetPresetCount, effects/IWMPEffects::GetPresetCount, wmp.iwmpeffects_getpresetcount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: effects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player version 7.0 or later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	effects.h
api_name:
-	IWMPEffects.GetPresetCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IWMPEffects::GetPresetCount


## -description



The <b>GetPresetCount</b> method gets the preset count.




## -parameters




### -param pnPresetCount






#### - count [out]

<b>Long</b> value specifying the preset count.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



Called by Windows Media Player to obtain the number of presets contained by the visualization.




## -see-also




<a href="https://msdn.microsoft.com/0f2a6bda-3e1f-4509-b8ff-ccf0909aa9ba">IWMPEffects Interface</a>
 

 

