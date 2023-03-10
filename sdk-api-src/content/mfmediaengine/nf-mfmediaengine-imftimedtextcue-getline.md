---
UID: NF:mfmediaengine.IMFTimedTextCue.GetLine
title: IMFTimedTextCue::GetLine (mfmediaengine.h)
description: Gets a line of text in the cue from the index of the line.
helpviewer_keywords: ["GetLine","GetLine method [Media Foundation]","GetLine method [Media Foundation]","IMFTimedTextCue interface","IMFTimedTextCue interface [Media Foundation]","GetLine method","IMFTimedTextCue.GetLine","IMFTimedTextCue::GetLine","mf.imftimedtextcue_getline","mfmediaengine/IMFTimedTextCue::GetLine"]
old-location: mf\imftimedtextcue_getline.htm
tech.root: mf
ms.assetid: CD29A63D-8D40-43E6-972C-7050E63EA7D3
ms.date: 12/05/2018
ms.keywords: GetLine, GetLine method [Media Foundation], GetLine method [Media Foundation],IMFTimedTextCue interface, IMFTimedTextCue interface [Media Foundation],GetLine method, IMFTimedTextCue.GetLine, IMFTimedTextCue::GetLine, mf.imftimedtextcue_getline, mfmediaengine/IMFTimedTextCue::GetLine
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
 - IMFTimedTextCue::GetLine
 - mfmediaengine/IMFTimedTextCue::GetLine
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
 - IMFTimedTextCue.GetLine
---

# IMFTimedTextCue::GetLine


## -description

Gets a line of text in the cue from the index of the line.

## -parameters

### -param index [in]

Type: <b>DWORD</b>

The index of the line of text in the cue to retrieve.

### -param line [out]

Type: <b><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextformattedtext">IMFTimedTextFormattedText</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextformattedtext">IMFTimedTextFormattedText</a> interface for the line of text in the cue.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextcue">IMFTimedTextCue</a>