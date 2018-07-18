---
UID: NF:qnetwork.IAMNetShowExProps.GetCodecDescription
title: IAMNetShowExProps::GetCodecDescription
author: windows-sdk-content
description: The GetCodecDescription method retrieves a user-friendly description of a specified codec.
old-location: dshow\iamnetshowexprops_getcodecdescription.htm
old-project: DirectShow
ms.assetid: 5a26e576-df4a-462d-8fab-0a133469e77b
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetCodecDescription, GetCodecDescription method [DirectShow], GetCodecDescription method [DirectShow],IAMNetShowExProps interface, IAMNetShowExProps interface [DirectShow],GetCodecDescription method, IAMNetShowExProps.GetCodecDescription, IAMNetShowExProps::GetCodecDescription, IAMNetShowExPropsGetCodecDescription, dshow.iamnetshowexprops_getcodecdescription, qnetwork/IAMNetShowExProps::GetCodecDescription
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: AMExtendedSeekingCapabilities
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetShowExProps.GetCodecDescription
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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




<a href="https://msdn.microsoft.com/e68959dc-1a79-4e2c-aeaf-3febcb9c09ce">IAMNetShowExProps Interface</a>



<a href="https://msdn.microsoft.com/7b16727d-565a-431e-8124-124d72816d65">IAMNetShowExProps::get_CodecCount</a>
 

 

