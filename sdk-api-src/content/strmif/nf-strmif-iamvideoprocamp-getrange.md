---
UID: NF:strmif.IAMVideoProcAmp.GetRange
title: IAMVideoProcAmp::GetRange (strmif.h)
description: The GetRange method gets the range and default value of a specified video property.helpviewer_keywords: ["GetRange","GetRange method [DirectShow]","GetRange method [DirectShow]","IAMVideoProcAmp interface","IAMVideoProcAmp interface [DirectShow]","GetRange method","IAMVideoProcAmp.GetRange","IAMVideoProcAmp::GetRange","IAMVideoProcAmpGetRange","dshow.iamvideoprocamp_getrange","strmif/IAMVideoProcAmp::GetRange"]
old-location: dshow\iamvideoprocamp_getrange.htm
tech.root: DirectShow
ms.assetid: 54e462a8-bb65-43e2-acf1-f0d64db2bf24
ms.date: 12/05/2018
ms.keywords: GetRange, GetRange method [DirectShow], GetRange method [DirectShow],IAMVideoProcAmp interface, IAMVideoProcAmp interface [DirectShow],GetRange method, IAMVideoProcAmp.GetRange, IAMVideoProcAmp::GetRange, IAMVideoProcAmpGetRange, dshow.iamvideoprocamp_getrange, strmif/IAMVideoProcAmp::GetRange
f1_keywords:
- strmif/IAMVideoProcAmp.GetRange
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
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
- IAMVideoProcAmp.GetRange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoProcAmp::GetRange


## -description



The <code>GetRange</code> method gets the range and default value of a specified video property.




## -parameters




### -param Property [in]

Specifies the property to query, as a value from the [VideoProcAmpProperty](https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-videoprocampproperty) enumeration.


### -param pMin [out]

Receives the minimum value of the property.
          


### -param pMax [out]

Receives the maximum value of the property.
          


### -param pSteppingDelta [out]

Receives the step size for the property. The step size is the smallest increment by which the property can change.
          


### -param pDefault [out]

Receives the default value of the property.
          


### -param pCapsFlags [out]

Receives a member of the [VideoProcAmpFlags](https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-videoprocampflags) enumeration, indicating whether the property is controlled automatically or manually.
          


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PROP_ID_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The device does not support this property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
No error.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/configure-the-video-quality">Configure the Video Quality</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamvideoprocamp">IAMVideoProcAmp Interface</a>
 

 

