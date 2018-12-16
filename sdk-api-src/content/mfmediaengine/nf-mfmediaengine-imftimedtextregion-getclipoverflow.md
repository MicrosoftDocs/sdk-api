---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetClipOverflow
title: IMFTimedTextRegion::GetClipOverflow
author: windows-sdk-content
description: Determines whether a clip of text overflowed the region.
old-location: mf\imftimedtextregion_getclipoverflow.htm
tech.root: medfound
ms.assetid: F48D4F1C-E00C-40BE-B292-B92C5B214F56
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetClipOverflow, GetClipOverflow method [Media Foundation], GetClipOverflow method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetClipOverflow method, IMFTimedTextRegion.GetClipOverflow, IMFTimedTextRegion::GetClipOverflow, mf.imftimedtextregion_getclipoverflow, mfmediaengine/IMFTimedTextRegion::GetClipOverflow
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
 - IMFTimedTextRegion.GetClipOverflow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextRegion::GetClipOverflow


## -description


Determines whether a clip of text overflowed the region.


## -parameters




### -param clipOverflow [out]

Type: <b>BOOL*</b>

A pointer to a variable that receives a value that specifies whether a clip of text overflowed the region. The variable specifies <b>TRUE</b> if the clip overflowed; otherwise, <b>FALSE</b>. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1A6E068F-2E01-4A72-8BCF-D645B1D21ECF">IMFTimedTextRegion</a>
 

 

