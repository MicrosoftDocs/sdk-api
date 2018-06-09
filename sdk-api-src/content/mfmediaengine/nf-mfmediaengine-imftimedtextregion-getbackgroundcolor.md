---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetBackgroundColor
title: IMFTimedTextRegion::GetBackgroundColor
author: windows-sdk-content
description: Gets the background color of the region.
old-location: mf\imftimedtextregion_getbackgroundcolor.htm
old-project: medfound
ms.assetid: E92FFB7E-C364-43C8-82CF-C3B4116C4187
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetBackgroundColor, GetBackgroundColor method [Media Foundation], GetBackgroundColor method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetBackgroundColor method, IMFTimedTextRegion.GetBackgroundColor, IMFTimedTextRegion::GetBackgroundColor, mf.imftimedtextregion_getbackgroundcolor, mfmediaengine/IMFTimedTextRegion::GetBackgroundColor
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MF_MEDIA_ENGINE_KEYERR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFTimedTextRegion.GetBackgroundColor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTimedTextRegion::GetBackgroundColor


## -description


Gets the background color of the region.


## -parameters




### -param bgColor






#### - pBgColor [out]

Type: <b><a href="https://msdn.microsoft.com/ce7ac174-9f00-42a4-9b48-ed86b406d83e">MFARGB</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/ce7ac174-9f00-42a4-9b48-ed86b406d83e">MFARGB</a> structure that describes the background color.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1A6E068F-2E01-4A72-8BCF-D645B1D21ECF">IMFTimedTextRegion</a>
 

 

