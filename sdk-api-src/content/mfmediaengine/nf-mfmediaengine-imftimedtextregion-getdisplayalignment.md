---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetDisplayAlignment
title: IMFTimedTextRegion::GetDisplayAlignment
author: windows-sdk-content
description: Gets the display alignment of the region.
old-location: mf\imftimedtextregion_getdisplayalignment.htm
tech.root: medfound
ms.assetid: CE2A9014-5510-4648-85F8-4A64C04C9F0C
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: GetDisplayAlignment, GetDisplayAlignment method [Media Foundation], GetDisplayAlignment method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetDisplayAlignment method, IMFTimedTextRegion.GetDisplayAlignment, IMFTimedTextRegion::GetDisplayAlignment, mf.imftimedtextregion_getdisplayalignment, mfmediaengine/IMFTimedTextRegion::GetDisplayAlignment
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
 - IMFTimedTextRegion.GetDisplayAlignment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextRegion::GetDisplayAlignment


## -description


Gets the display alignment of the region.


## -parameters




### -param displayAlign

TBD




#### - pDisplayAlign [out]

Type: <b><a href="https://msdn.microsoft.com/CB7C4067-7410-4F20-A6E8-8DED44AF5C83">MF_TIMED_TEXT_DISPLAY_ALIGNMENT</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/CB7C4067-7410-4F20-A6E8-8DED44AF5C83">MF_TIMED_TEXT_DISPLAY_ALIGNMENT</a>-typed value that specifies the display alignment of the region.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1A6E068F-2E01-4A72-8BCF-D645B1D21ECF">IMFTimedTextRegion</a>
 

 

