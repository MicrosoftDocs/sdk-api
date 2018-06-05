---
UID: NF:strmif.IEncoderAPI.SetValue
title: IEncoderAPI::SetValue
author: windows-sdk-content
description: The SetValue method sets the current value of a parameter.
old-location: mstv\iencoderapi_setvalue.htm
old-project: mstv
ms.assetid: a7dc0964-64b9-4ea3-8948-19ec100d64f5
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IEncoderAPI interface [Microsoft TV Technologies],SetValue method, IEncoderAPI.SetValue, IEncoderAPI::SetValue, IEncoderAPISetValue, SetValue, SetValue method [Microsoft TV Technologies], SetValue method [Microsoft TV Technologies],IEncoderAPI interface, mstv.iencoderapi_setvalue, strmif/IEncoderAPI::SetValue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IEncoderAPI.SetValue
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IEncoderAPI::SetValue


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/823b79a1-1bf5-4aab-80dd-0e77ba950127">IEncoderAPI</a> is no longer available for use. Instead, use <a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a>.]

The <b>SetValue</b> method sets the current value of a parameter.


## -parameters




### -param Api [in]


            Pointer to a GUID that specifies the parameter.
          


### -param Value [out]


            Pointer that specifies the value of <i>Api</i>. If <i>Api</i> was specified as <b>ENCAPIPARAM_BITRATE_MODE</b>, then <i>Value</i> must be one of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568695">VIDEOENCODER_BITRATE_MODE</a> constants.
            
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>



<a href="https://msdn.microsoft.com/823b79a1-1bf5-4aab-80dd-0e77ba950127">IEncoderAPI Interface</a>
 

 

