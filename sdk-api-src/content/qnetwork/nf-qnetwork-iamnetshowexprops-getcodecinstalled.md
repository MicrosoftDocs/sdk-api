---
UID: NF:qnetwork.IAMNetShowExProps.GetCodecInstalled
title: IAMNetShowExProps::GetCodecInstalled (qnetwork.h)
description: The GetCodecInstalled method queries whether a specified codec is installed on the local system.
helpviewer_keywords: ["GetCodecInstalled","GetCodecInstalled method [DirectShow]","GetCodecInstalled method [DirectShow]","IAMNetShowExProps interface","IAMNetShowExProps interface [DirectShow]","GetCodecInstalled method","IAMNetShowExProps.GetCodecInstalled","IAMNetShowExProps::GetCodecInstalled","IAMNetShowExPropsGetCodecInstalled","dshow.iamnetshowexprops_getcodecinstalled","qnetwork/IAMNetShowExProps::GetCodecInstalled"]
old-location: dshow\iamnetshowexprops_getcodecinstalled.htm
tech.root: dshow
ms.assetid: 597178a5-8ead-4562-adbe-e6cd2b352d25
ms.date: 12/05/2018
ms.keywords: GetCodecInstalled, GetCodecInstalled method [DirectShow], GetCodecInstalled method [DirectShow],IAMNetShowExProps interface, IAMNetShowExProps interface [DirectShow],GetCodecInstalled method, IAMNetShowExProps.GetCodecInstalled, IAMNetShowExProps::GetCodecInstalled, IAMNetShowExPropsGetCodecInstalled, dshow.iamnetshowexprops_getcodecinstalled, qnetwork/IAMNetShowExProps::GetCodecInstalled
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IAMNetShowExProps::GetCodecInstalled
 - qnetwork/IAMNetShowExProps::GetCodecInstalled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetShowExProps.GetCodecInstalled
---

# IAMNetShowExProps::GetCodecInstalled


## -description

The <code>GetCodecInstalled</code> method queries whether a specified codec is installed on the local system.

## -parameters

### -param CodecNum

Specifies the codec to query, indexed from zero. Call <b>get_CodecCount</b> to obtain the number of codecs.

### -param pCodecInstalled

Pointer that receives a Boolean value.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowexprops">IAMNetShowExProps Interface</a>



<a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowexprops-get_codeccount">IAMNetShowExProps::get_CodecCount</a>