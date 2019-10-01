---
UID: NF:qnetwork.IAMNetShowExProps.GetCodecDescription
title: IAMNetShowExProps::GetCodecDescription (qnetwork.h)
author: windows-sdk-content
description: The GetCodecDescription method retrieves a user-friendly description of a specified codec.
old-location: dshow\iamnetshowexprops_getcodecdescription.htm
tech.root: DirectShow
ms.assetid: 5a26e576-df4a-462d-8fab-0a133469e77b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCodecDescription, GetCodecDescription method [DirectShow], GetCodecDescription method [DirectShow],IAMNetShowExProps interface, IAMNetShowExProps interface [DirectShow],GetCodecDescription method, IAMNetShowExProps.GetCodecDescription, IAMNetShowExProps::GetCodecDescription, IAMNetShowExPropsGetCodecDescription, dshow.iamnetshowexprops_getcodecdescription, qnetwork/IAMNetShowExProps::GetCodecDescription
ms.topic: method
f1_keywords: 
 - "qnetwork/IAMNetShowExProps.GetCodecDescription"
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
 - IAMNetShowExProps.GetCodecDescription
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMNetShowExProps::GetCodecDescription


## -description



The <code>GetCodecDescription</code> method retrieves a user-friendly description of a specified codec.




## -parameters




### -param CodecNum

Specifies the codec to query, indexed from zero. Call <b>get_CodecCount</b> to obtain the number of codecs.


### -param pbstrCodecDescription

Pointer to a variable that receives the description.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The caller must release the returned <b>BSTR</b>, by calling <b>SysFreeString</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowexprops">IAMNetShowExProps Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowexprops-get_codeccount">IAMNetShowExProps::get_CodecCount</a>
 

 

