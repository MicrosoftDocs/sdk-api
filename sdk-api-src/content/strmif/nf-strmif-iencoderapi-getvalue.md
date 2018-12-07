---
UID: NF:strmif.IEncoderAPI.GetValue
title: IEncoderAPI::GetValue
author: windows-sdk-content
description: The GetValue method retrieves the current value of a specified parameter.
old-location: mstv\iencoderapi_getvalue.htm
tech.root: mstv
ms.assetid: 62f69677-05cd-46ab-8b77-96e10f8fbb1d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetValue, GetValue method [Microsoft TV Technologies], GetValue method [Microsoft TV Technologies],IEncoderAPI interface, IEncoderAPI interface [Microsoft TV Technologies],GetValue method, IEncoderAPI.GetValue, IEncoderAPI::GetValue, IEncoderAPIGetValue, mstv.iencoderapi_getvalue, strmif/IEncoderAPI::GetValue
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IEncoderAPI.GetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEncoderAPI::GetValue


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/823b79a1-1bf5-4aab-80dd-0e77ba950127">IEncoderAPI</a> is no longer available for use. Instead, use <a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a>.]

The <b>GetValue</b> method retrieves the current value of a specified parameter.


## -parameters




### -param Api [in]

Pointer to a GUID that specifies the parameter.
          


### -param Value [out]

Receives the value for the parameter specified in <i>Api</i>. If <i>Api</i> was specified as ENCAPIPARAM_BITRATE_MODE, then <i>Value</i> will be one of the <a href="https://msdn.microsoft.com/ccceae9a-6d1d-4453-bd84-88cefc20320e">VIDEOENCODER_BITRATE_MODE</a> constants.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>



<a href="https://msdn.microsoft.com/823b79a1-1bf5-4aab-80dd-0e77ba950127">IEncoderAPI Interface</a>
 

 

