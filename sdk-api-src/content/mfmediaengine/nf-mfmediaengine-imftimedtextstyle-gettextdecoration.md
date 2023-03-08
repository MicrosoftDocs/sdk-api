---
UID: NF:mfmediaengine.IMFTimedTextStyle.GetTextDecoration
title: IMFTimedTextStyle::GetTextDecoration (mfmediaengine.h)
description: Gets how text is decorated for the timed-text style.
helpviewer_keywords: ["GetTextDecoration","GetTextDecoration method [Media Foundation]","GetTextDecoration method [Media Foundation]","IMFTimedTextStyle interface","IMFTimedTextStyle interface [Media Foundation]","GetTextDecoration method","IMFTimedTextStyle.GetTextDecoration","IMFTimedTextStyle::GetTextDecoration","mf.imftimedtextstyle_gettextdecoration","mfmediaengine/IMFTimedTextStyle::GetTextDecoration"]
old-location: mf\imftimedtextstyle_gettextdecoration.htm
tech.root: mf
ms.assetid: 5B987C19-5F59-4B5D-BA40-341FA4B3CD35
ms.date: 12/05/2018
ms.keywords: GetTextDecoration, GetTextDecoration method [Media Foundation], GetTextDecoration method [Media Foundation],IMFTimedTextStyle interface, IMFTimedTextStyle interface [Media Foundation],GetTextDecoration method, IMFTimedTextStyle.GetTextDecoration, IMFTimedTextStyle::GetTextDecoration, mf.imftimedtextstyle_gettextdecoration, mfmediaengine/IMFTimedTextStyle::GetTextDecoration
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTimedTextStyle::GetTextDecoration
 - mfmediaengine/IMFTimedTextStyle::GetTextDecoration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFTimedTextStyle.GetTextDecoration
---

# IMFTimedTextStyle::GetTextDecoration


## -description

Gets how text is decorated for the timed-text style.

## -parameters

### -param textDecoration [out]

Type: <b>DWORD*</b>

A pointer to a variable that receives a combination of <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_decoration">MF_TIMED_TEXT_DECORATION</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies how text is decorated.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle">IMFTimedTextStyle</a>