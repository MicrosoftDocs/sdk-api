---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetLineHeight
title: IMFTimedTextRegion::GetLineHeight (mfmediaengine.h)

description: Gets the height of each line of text in the region.
old-location: mf\imftimedtextregion_getlineheight.htm
tech.root: medfound
ms.assetid: 41514FCA-5C2A-48E5-A9F8-72B5B9160CD6

ms.date: 12/05/2018
ms.keywords: GetLineHeight, GetLineHeight method [Media Foundation], GetLineHeight method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetLineHeight method, IMFTimedTextRegion.GetLineHeight, IMFTimedTextRegion::GetLineHeight, mf.imftimedtextregion_getlineheight, mfmediaengine/IMFTimedTextRegion::GetLineHeight
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFTimedTextRegion.GetLineHeight"
dev_langs:
 - c++
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
 - IMFTimedTextRegion.GetLineHeight
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextRegion::GetLineHeight


## -description


Gets the height of each line of text in the region.


## -parameters




### -param pLineHeight [out]

Type: <b>double*</b>

A pointer to a variable that receives the height of each line of text in the region.


### -param unitType [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_unit_type">MF_TIMED_TEXT_UNIT_TYPE</a>*</b>

A pointer to a variable that receives a <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_unit_type">MF_TIMED_TEXT_UNIT_TYPE</a>-typed value that specifies the units in which the timed-text region is measured.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion">IMFTimedTextRegion</a>
 

 

