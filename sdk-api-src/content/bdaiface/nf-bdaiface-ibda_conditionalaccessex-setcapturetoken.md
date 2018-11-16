---
UID: NF:bdaiface.IBDA_ConditionalAccessEx.SetCaptureToken
title: IBDA_ConditionalAccessEx::SetCaptureToken
author: windows-sdk-content
description: Requests special events that are identified by a capture token.
old-location: mstv\ibda_conditionalaccessex_setcapturetoken.htm
tech.root: mstv
ms.assetid: b9e3d319-c76c-45df-aca3-d5447605b7c0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IBDA_ConditionalAccessEx interface [Microsoft TV Technologies],SetCaptureToken method, IBDA_ConditionalAccessEx.SetCaptureToken, IBDA_ConditionalAccessEx::SetCaptureToken, SetCaptureToken, SetCaptureToken method [Microsoft TV Technologies], SetCaptureToken method [Microsoft TV Technologies],IBDA_ConditionalAccessEx interface, bdaiface/IBDA_ConditionalAccessEx::SetCaptureToken, mstv.ibda_conditionalaccessex_setcapturetoken
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_ConditionalAccessEx.SetCaptureToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- bdaiface.h
: 
- IBDA_ConditionalAccessEx.SetCaptureToken
: 
---

# IBDA_ConditionalAccessEx::SetCaptureToken


## -description


Requests special events that are identified by a capture token.

A <i>capture token</i> is a binary blob that indicates a specific purchase option for content.


## -parameters




### -param ulcbCaptureTokenLen [in]

The size, in bytes, of the <i>pbCaptureToken</i> array.


### -param pbCaptureToken [in]

Pointer to a byte array that contains the capture token.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9db9b6b1-fc4f-48f0-940e-d79a321ef094">IBDA_ConditionalAccessEx</a>
 

 

