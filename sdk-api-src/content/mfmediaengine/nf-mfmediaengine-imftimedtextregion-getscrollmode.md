---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetScrollMode
title: IMFTimedTextRegion::GetScrollMode
author: windows-sdk-content
description: Gets the scroll mode of the region.
old-location: mf\imftimedtextregion_getscrollmode.htm
tech.root: medfound
ms.assetid: 85CD2A7A-23ED-4D5C-AAEC-D5DF9F059897
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetScrollMode, GetScrollMode method [Media Foundation], GetScrollMode method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetScrollMode method, IMFTimedTextRegion.GetScrollMode, IMFTimedTextRegion::GetScrollMode, mf.imftimedtextregion_getscrollmode, mfmediaengine/IMFTimedTextRegion::GetScrollMode
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFTimedTextRegion.GetScrollMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextRegion::GetScrollMode


## -description


Gets the scroll mode of the region.


## -parameters




### -param scrollMode [out]

Type: <b><a href="https://msdn.microsoft.com/7FE9B5BB-7313-4E9F-A34E-FDFBC6F07686">MF_TIMED_TEXT_SCROLL_MODE</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/7FE9B5BB-7313-4E9F-A34E-FDFBC6F07686">MF_TIMED_TEXT_SCROLL_MODE</a>-typed value that specifies the scroll mode of the region.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1A6E068F-2E01-4A72-8BCF-D645B1D21ECF">IMFTimedTextRegion</a>
 

 

