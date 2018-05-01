---
UID: NF:qnetwork.IAMNetShowExProps.GetCodecDescription
title: IAMNetShowExProps::GetCodecDescription method
author: windows-driver-content
description: The GetCodecDescription method retrieves a user-friendly description of a specified codec.
old-location: dshow\iamnetshowexprops_getcodecdescription.htm
old-project: DirectShow
ms.assetid: 5a26e576-df4a-462d-8fab-0a133469e77b
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetCodecDescription method [DirectShow], GetCodecDescription method [DirectShow], IAMNetShowExProps interface, GetCodecDescription,IAMNetShowExProps.GetCodecDescription, IAMNetShowExProps, IAMNetShowExProps interface [DirectShow], GetCodecDescription method, IAMNetShowExProps::GetCodecDescription, IAMNetShowExPropsGetCodecDescription, dshow.iamnetshowexprops_getcodecdescription, qnetwork/IAMNetShowExProps::GetCodecDescription
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AMExtendedSeekingCapabilities
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Qnetwork.h
api_name:
-	IAMNetShowExProps.GetCodecDescription
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IAMNetShowExProps::GetCodecDescription method


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
 

 

