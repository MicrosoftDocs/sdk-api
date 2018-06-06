---
UID: NF:strmif.IEncoderAPI.GetDefaultValue
title: IEncoderAPI::GetDefaultValue
author: windows-sdk-content
description: The GetDefaultValue method retrieves the default value for a parameter, if one exists.
old-location: mstv\iencoderapi_getdefaultvalue.htm
old-project: mstv
ms.assetid: 86eb8008-6d1c-4de7-8a88-b42f33ca24d3
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetDefaultValue, GetDefaultValue method [Microsoft TV Technologies], GetDefaultValue method [Microsoft TV Technologies],IEncoderAPI interface, IEncoderAPI interface [Microsoft TV Technologies],GetDefaultValue method, IEncoderAPI.GetDefaultValue, IEncoderAPI::GetDefaultValue, IEncoderAPIGetDefaultValue, mstv.iencoderapi_getdefaultvalue, strmif/IEncoderAPI::GetDefaultValue
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IEncoderAPI.GetDefaultValue
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IEncoderAPI::GetDefaultValue


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/823b79a1-1bf5-4aab-80dd-0e77ba950127">IEncoderAPI</a> is no longer available for use. Instead, use <a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a>.]

The <b>GetDefaultValue</b> method retrieves the default value for a parameter, if one exists.


## -parameters




### -param Api [in]


            Pointer to a GUID that specifies the parameter.
          


### -param Value [out]


            Receives the value for the parameter specified in <i>Api</i>. If <i>Api</i> was specified as ENCAPIPARAM_BITRATE_MODE, then <i>Value</i> will be one of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568695">VIDEOENCODER_BITRATE_MODE</a> constants.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>



<a href="https://msdn.microsoft.com/823b79a1-1bf5-4aab-80dd-0e77ba950127">IEncoderAPI Interface</a>
 

 

