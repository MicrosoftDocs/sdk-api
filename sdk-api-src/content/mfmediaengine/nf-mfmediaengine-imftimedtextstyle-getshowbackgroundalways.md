---
UID: NF:mfmediaengine.IMFTimedTextStyle.GetShowBackgroundAlways
title: IMFTimedTextStyle::GetShowBackgroundAlways method
author: windows-driver-content
description: Determines whether the style of timed text always shows the background.
old-location: mf\imftimedtextstyle_getshowbackgroundalways.htm
old-project: medfound
ms.assetid: 3FE2327F-542B-45D3-95F4-09CF0CE26403
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: GetShowBackgroundAlways method [Media Foundation], GetShowBackgroundAlways method [Media Foundation], IMFTimedTextStyle interface, GetShowBackgroundAlways,IMFTimedTextStyle.GetShowBackgroundAlways, IMFTimedTextStyle, IMFTimedTextStyle interface [Media Foundation], GetShowBackgroundAlways method, IMFTimedTextStyle::GetShowBackgroundAlways, mf.imftimedtextstyle_getshowbackgroundalways, mfmediaengine/IMFTimedTextStyle::GetShowBackgroundAlways
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFTimedTextStyle.GetShowBackgroundAlways
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTimedTextStyle::GetShowBackgroundAlways method


## -description


Determines whether the style  of timed text always shows the background.


## -parameters




### -param showBackgroundAlways






#### - pfShowBackgroundAlways [out]

Type: <b>BOOL*</b>

A pointer to a variable that receives a value that specifies whether the style  of timed text always shows the background. The variable specifies <b>TRUE</b> if the background is always shown; otherwise, <b>FALSE</b>. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ED358A36-BEEF-491E-8984-938F71472F26">IMFTimedTextStyle</a>
 

 

