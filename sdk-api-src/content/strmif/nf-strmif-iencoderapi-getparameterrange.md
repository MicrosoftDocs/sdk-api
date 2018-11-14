---
UID: NF:strmif.IEncoderAPI.GetParameterRange
title: IEncoderAPI::GetParameterRange
author: windows-sdk-content
description: The GetParameterRange method retrieves the valid range of values that the parameter supports, in cases where the parameter supports a stepped range as opposed to a list of specific values.
old-location: mstv\iencoderapi_getparameterrange.htm
tech.root: MSTV
ms.assetid: fb48a460-c891-4fbe-8fe2-f900f8b405b7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetParameterRange, GetParameterRange method [Microsoft TV Technologies], GetParameterRange method [Microsoft TV Technologies],IEncoderAPI interface, IEncoderAPI interface [Microsoft TV Technologies],GetParameterRange method, IEncoderAPI.GetParameterRange, IEncoderAPI::GetParameterRange, IEncoderAPIGetParameterRange, mstv.iencoderapi_getparameterrange, strmif/IEncoderAPI::GetParameterRange
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
 - IEncoderAPI.GetParameterRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IEncoderAPI.GetParameterRange
: 
---

# IEncoderAPI::GetParameterRange


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/823b79a1-1bf5-4aab-80dd-0e77ba950127">IEncoderAPI</a> is no longer available for use. Instead, use <a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a>.]

The <b>GetParameterRange</b> method retrieves the valid range of values that the parameter supports, in cases where the parameter supports a stepped range as opposed to a list of specific values.


## -parameters




### -param Api [in]

Pointer to a GUID that specifies the parameter.
          


### -param ValueMin [out]

Pointer to a <b>VARIANT</b> type that receives the minimum value of the parameter.
          


### -param ValueMax [out]

Pointer to a <b>VARIANT</b> type that receives the maximum value of the parameter.
          


### -param SteppingDelta [out]

Pointer to a <b>VARIANT</b> type that receives the stepping delta, which defines the valid increments from <i>ValueMin</i> to <i>ValueMax</i>.
          


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The property supports a list of possible values, not a linear range.

</td>
</tr>
</table>
 




## -remarks



The valid range for the parameter is [<i>ValueMax</i>...<i>ValueMax</i>], with increments of <i>SteppingDelta</i>. If a parameter supports a stepped range of values, it must use one of the following variant types:

<ul>
<li>Unsigned types : <b>VT_UI8</b>, <b>VT_UI4</b>, <b>VT_UI2</b>, <b>VT_UI1</b></li>
<li>Signed types : <b>VT_I8</b>, <b>VT_I4</b>, <b>VT_I2</b></li>
<li>Float types : <b>VT_R8</b>, <b>VT_R4</b></li>
</ul>
By definition, the parameter will return a specific type.
      

Any stepping value is valid. If the range has no stepping delta (that is, you can increment by any value), the encoder should return an empty value (<b>VT_EMPTY</b>) for <i>SteppingDelta</i>.
      

If <i>Api</i> equals <b>ENCAPIPARAM_BITRATE_MODE</b>, the method returns <b>E_NOTIMPL</b>, because the bitrate mode constants are a list of specific values.
      




## -see-also




<a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>



<a href="https://msdn.microsoft.com/823b79a1-1bf5-4aab-80dd-0e77ba950127">IEncoderAPI Interface</a>
 

 

