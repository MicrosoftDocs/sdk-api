---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# IMFTimedTextRegion::GetScrollMode


## -description


Gets the scroll mode of the region.


## -parameters




### -param scrollMode






#### - pScrollMode [out]

Type: <b><a href="https://msdn.microsoft.com/7FE9B5BB-7313-4E9F-A34E-FDFBC6F07686">MF_TIMED_TEXT_SCROLL_MODE</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/7FE9B5BB-7313-4E9F-A34E-FDFBC6F07686">MF_TIMED_TEXT_SCROLL_MODE</a>-typed value that specifies the scroll mode of the region.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1A6E068F-2E01-4A72-8BCF-D645B1D21ECF">IMFTimedTextRegion</a>
 

 

