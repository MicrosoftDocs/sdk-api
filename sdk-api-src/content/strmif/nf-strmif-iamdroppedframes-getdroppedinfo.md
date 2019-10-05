---
UID: NF:strmif.IAMDroppedFrames.GetDroppedInfo
title: IAMDroppedFrames::GetDroppedInfo (strmif.h)
author: windows-sdk-content
description: The GetDroppedInfo method retrieves an array of frame numbers that were dropped.
old-location: dshow\iamdroppedframes_getdroppedinfo.htm
tech.root: DirectShow
ms.assetid: d4dc9e68-f814-4bb4-88ea-88eea32b2577
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDroppedInfo, GetDroppedInfo method [DirectShow], GetDroppedInfo method [DirectShow],IAMDroppedFrames interface, IAMDroppedFrames interface [DirectShow],GetDroppedInfo method, IAMDroppedFrames.GetDroppedInfo, IAMDroppedFrames::GetDroppedInfo, IAMDroppedFramesGetDroppedInfo, dshow.iamdroppedframes_getdroppedinfo, strmif/IAMDroppedFrames::GetDroppedInfo
ms.topic: method
f1_keywords: 
 - "strmif/IAMDroppedFrames.GetDroppedInfo"
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
 - IAMDroppedFrames.GetDroppedInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMDroppedFrames::GetDroppedInfo


## -description



The <code>GetDroppedInfo</code> method retrieves an array of frame numbers that were dropped.




## -parameters




### -param lSize [in]

Specifies the size of the array.


### -param plArray [out]

Pointer to an array of size <i>lSize</i>, allocated by the caller. The method fills the array with the frame numbers of the first <i>lSize</i> frames that were dropped, up to a maximum number that is device-depedent.


### -param plNumCopied [out]

Pointer to a variable that receives the number of items returned in <i>plArray</i>. This number might be less than the value of <i>lSize</i>.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument; the <i>lSize</i> parameter must by greater than zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

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
Not supported by this device.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamdroppedframes">IAMDroppedFrames Interface</a>
 

 

