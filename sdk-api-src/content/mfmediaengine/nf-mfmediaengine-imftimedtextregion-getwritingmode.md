---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetWritingMode
title: IMFTimedTextRegion::GetWritingMode
author: windows-sdk-content
description: Gets the writing mode of the region.
old-location: mf\imftimedtextregion_getwritingmode.htm
old-project: medfound
ms.assetid: BCF99D3C-554A-4788-B54B-236F463B1EAE
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetWritingMode, GetWritingMode method [Media Foundation], GetWritingMode method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetWritingMode method, IMFTimedTextRegion.GetWritingMode, IMFTimedTextRegion::GetWritingMode, mf.imftimedtextregion_getwritingmode, mfmediaengine/IMFTimedTextRegion::GetWritingMode
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
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFTimedTextRegion.GetWritingMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTimedTextRegion::GetWritingMode


## -description


Gets the writing mode of the region.


## -parameters




### -param writingMode






#### - pWritingMode [out]

Type: <b><a href="https://msdn.microsoft.com/AE77AC07-EA27-4341-97E4-7D0995AF18E8">MF_TIMED_TEXT_WRITING_MODE</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/AE77AC07-EA27-4341-97E4-7D0995AF18E8">MF_TIMED_TEXT_WRITING_MODE</a>-typed value that specifies the writing mode of the region.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1A6E068F-2E01-4A72-8BCF-D645B1D21ECF">IMFTimedTextRegion</a>
 

 

