---
UID: NF:qnetwork.IAMNetShowExProps.GetCodecInstalled
title: IAMNetShowExProps::GetCodecInstalled (qnetwork.h)
author: windows-sdk-content
description: The GetCodecInstalled method queries whether a specified codec is installed on the local system.
old-location: dshow\iamnetshowexprops_getcodecinstalled.htm
tech.root: DirectShow
ms.assetid: 597178a5-8ead-4562-adbe-e6cd2b352d25
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCodecInstalled, GetCodecInstalled method [DirectShow], GetCodecInstalled method [DirectShow],IAMNetShowExProps interface, IAMNetShowExProps interface [DirectShow],GetCodecInstalled method, IAMNetShowExProps.GetCodecInstalled, IAMNetShowExProps::GetCodecInstalled, IAMNetShowExPropsGetCodecInstalled, dshow.iamnetshowexprops_getcodecinstalled, qnetwork/IAMNetShowExProps::GetCodecInstalled
ms.topic: method
f1_keywords: 
 - "qnetwork/IAMNetShowExProps.GetCodecInstalled"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetShowExProps.GetCodecInstalled
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowexprops">IAMNetShowExProps Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowexprops-get_codeccount">IAMNetShowExProps::get_CodecCount</a>
 

 

