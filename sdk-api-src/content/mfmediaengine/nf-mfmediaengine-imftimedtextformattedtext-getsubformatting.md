---
UID: NF:mfmediaengine.IMFTimedTextFormattedText.GetSubformatting
title: IMFTimedTextFormattedText::GetSubformatting (mfmediaengine.h)
description: Gets a subformat in the formatted timed-text object.
helpviewer_keywords: ["GetSubformatting","GetSubformatting method [Media Foundation]","GetSubformatting method [Media Foundation]","IMFTimedTextFormattedText interface","IMFTimedTextFormattedText interface [Media Foundation]","GetSubformatting method","IMFTimedTextFormattedText.GetSubformatting","IMFTimedTextFormattedText::GetSubformatting","mf.imftimedtextformattedtext_getsubformatting","mfmediaengine/IMFTimedTextFormattedText::GetSubformatting"]
old-location: mf\imftimedtextformattedtext_getsubformatting.htm
tech.root: mf
ms.assetid: EC6F41A4-BB07-419B-BE03-8D82709D9A24
ms.date: 12/05/2018
ms.keywords: GetSubformatting, GetSubformatting method [Media Foundation], GetSubformatting method [Media Foundation],IMFTimedTextFormattedText interface, IMFTimedTextFormattedText interface [Media Foundation],GetSubformatting method, IMFTimedTextFormattedText.GetSubformatting, IMFTimedTextFormattedText::GetSubformatting, mf.imftimedtextformattedtext_getsubformatting, mfmediaengine/IMFTimedTextFormattedText::GetSubformatting
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
 - IMFTimedTextFormattedText::GetSubformatting
 - mfmediaengine/IMFTimedTextFormattedText::GetSubformatting
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
 - IMFTimedTextFormattedText.GetSubformatting
---

# IMFTimedTextFormattedText::GetSubformatting


## -description

Gets a subformat in the formatted timed-text object.

## -parameters

### -param index [in]

Type: <b>DWORD</b>

The index of the subformat in the formatted timed-text object.

### -param firstChar [out]

Type: <b>DWORD*</b>

A pointer to a variable that receives the first character of the subformat.

### -param charLength [out]

Type: <b>DWORD*</b>

A pointer to a variable that receives the length, in characters, of the subformat.

### -param style [out]

Type: <b><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle">IMFTimedTextStyle</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle">IMFTimedTextStyle</a> interface for the subformat's timed-text style. This parameter can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextformattedtext">IMFTimedTextFormattedText</a>