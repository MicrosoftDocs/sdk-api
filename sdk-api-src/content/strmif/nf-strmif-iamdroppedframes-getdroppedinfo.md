---
UID: NF:strmif.IAMDroppedFrames.GetDroppedInfo
title: IAMDroppedFrames::GetDroppedInfo method
author: windows-driver-content
description: The GetDroppedInfo method retrieves an array of frame numbers that were dropped.
old-location: dshow\iamdroppedframes_getdroppedinfo.htm
old-project: DirectShow
ms.assetid: d4dc9e68-f814-4bb4-88ea-88eea32b2577
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetDroppedInfo method [DirectShow], GetDroppedInfo method [DirectShow], IAMDroppedFrames interface, GetDroppedInfo,IAMDroppedFrames.GetDroppedInfo, IAMDroppedFrames, IAMDroppedFrames interface [DirectShow], GetDroppedInfo method, IAMDroppedFrames::GetDroppedInfo, IAMDroppedFramesGetDroppedInfo, dshow.iamdroppedframes_getdroppedinfo, strmif/IAMDroppedFrames::GetDroppedInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
-	IAMDroppedFrames.GetDroppedInfo
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMDroppedFrames::GetDroppedInfo method


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b41c3792-76fe-48e0-b2f5-ca3b0ee4c8ae">IAMDroppedFrames Interface</a>
 

 

