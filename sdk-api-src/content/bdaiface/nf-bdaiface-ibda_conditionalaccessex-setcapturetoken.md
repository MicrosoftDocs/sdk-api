---
UID: NF:bdaiface.IBDA_ConditionalAccessEx.SetCaptureToken
title: IBDA_ConditionalAccessEx::SetCaptureToken (bdaiface.h)
description: Requests special events that are identified by a capture token.
helpviewer_keywords: ["IBDA_ConditionalAccessEx interface [Microsoft TV Technologies]","SetCaptureToken method","IBDA_ConditionalAccessEx.SetCaptureToken","IBDA_ConditionalAccessEx::SetCaptureToken","SetCaptureToken","SetCaptureToken method [Microsoft TV Technologies]","SetCaptureToken method [Microsoft TV Technologies]","IBDA_ConditionalAccessEx interface","bdaiface/IBDA_ConditionalAccessEx::SetCaptureToken","mstv.ibda_conditionalaccessex_setcapturetoken"]
old-location: mstv\ibda_conditionalaccessex_setcapturetoken.htm
tech.root: mstv
ms.assetid: b9e3d319-c76c-45df-aca3-d5447605b7c0
ms.date: 12/05/2018
ms.keywords: IBDA_ConditionalAccessEx interface [Microsoft TV Technologies],SetCaptureToken method, IBDA_ConditionalAccessEx.SetCaptureToken, IBDA_ConditionalAccessEx::SetCaptureToken, SetCaptureToken, SetCaptureToken method [Microsoft TV Technologies], SetCaptureToken method [Microsoft TV Technologies],IBDA_ConditionalAccessEx interface, bdaiface/IBDA_ConditionalAccessEx::SetCaptureToken, mstv.ibda_conditionalaccessex_setcapturetoken
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
 - IBDA_ConditionalAccessEx::SetCaptureToken
 - bdaiface/IBDA_ConditionalAccessEx::SetCaptureToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_ConditionalAccessEx.SetCaptureToken
---

# IBDA_ConditionalAccessEx::SetCaptureToken


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Requests special events that are identified by a capture token.

A <i>capture token</i> is a binary blob that indicates a specific purchase option for content.

## -parameters

### -param ulcbCaptureTokenLen [in]

The size, in bytes, of the <i>pbCaptureToken</i> array.

### -param pbCaptureToken [in]

Pointer to a byte array that contains the capture token.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_conditionalaccessex">IBDA_ConditionalAccessEx</a>