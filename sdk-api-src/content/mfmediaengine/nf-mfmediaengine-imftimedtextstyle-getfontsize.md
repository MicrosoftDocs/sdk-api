---
UID: NF:mfmediaengine.IMFTimedTextStyle.GetFontSize
title: IMFTimedTextStyle::GetFontSize (mfmediaengine.h)
author: windows-sdk-content
description: Gets the font size of the timed-text style.
old-location: mf\imftimedtextstyle_getfontsize.htm
tech.root: medfound
ms.assetid: A640F042-80BE-4454-B974-F7D076E72737
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFontSize, GetFontSize method [Media Foundation], GetFontSize method [Media Foundation],IMFTimedTextStyle interface, IMFTimedTextStyle interface [Media Foundation],GetFontSize method, IMFTimedTextStyle.GetFontSize, IMFTimedTextStyle::GetFontSize, mf.imftimedtextstyle_getfontsize, mfmediaengine/IMFTimedTextStyle::GetFontSize
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFTimedTextStyle.GetFontSize"
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
 - IMFTimedTextStyle.GetFontSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextStyle::GetFontSize


## -description


Gets the font size  of the timed-text style.


## -parameters




### -param fontSize [out]

Type: <b>double*</b>

A pointer to a variable that receives the font size  of the timed-text style.


### -param unitType [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_unit_type">MF_TIMED_TEXT_UNIT_TYPE</a>*</b>

A pointer to a variable that receives a <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_unit_type">MF_TIMED_TEXT_UNIT_TYPE</a>-typed value that specifies the units in which the timed-text style is measured.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle">IMFTimedTextStyle</a>
 

 

