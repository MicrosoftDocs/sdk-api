---
UID: NF:iwstdec.IAMWstDecoder.SetAnswerMode
title: IAMWstDecoder::SetAnswerMode
author: windows-sdk-content
description: Downstream filters use the SetAnswerMode method to assign the current answer mode.
old-location: dshow\iamwstdecoder_setanswermode.htm
tech.root: DirectShow
ms.assetid: d26b22d2-2c88-4347-80fb-aca8abae50ab
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAMWstDecoder interface [DirectShow],SetAnswerMode method, IAMWstDecoder.SetAnswerMode, IAMWstDecoder::SetAnswerMode, IAMWstDecoderSetAnswerMode, SetAnswerMode, SetAnswerMode method [DirectShow], SetAnswerMode method [DirectShow],IAMWstDecoder interface, dshow.iamwstdecoder_setanswermode, iwstdec/IAMWstDecoder::SetAnswerMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: iwstdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMWstDecoder.SetAnswerMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMWstDecoder::SetAnswerMode


## -description



Downstream filters use the <code>SetAnswerMode</code> method to assign the current answer mode.




## -parameters




### -param bAnswer [in]

Specifies the current answer mode.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Hidden text exposed.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Hidden text not exposed.</td>
</tr>
</table>
 


## -returns



When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/f2f5a459-14de-4be1-909c-3c23e4cfd737">IAMWstDecoder Interface</a>
 

 

