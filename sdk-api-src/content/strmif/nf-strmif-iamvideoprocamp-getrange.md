---
UID: NF:strmif.IAMVideoProcAmp.GetRange
title: IAMVideoProcAmp::GetRange method
author: windows-driver-content
description: The GetRange method gets the range and default value of a specified video property.
old-location: dshow\iamvideoprocamp_getrange.htm
old-project: DirectShow
ms.assetid: 54e462a8-bb65-43e2-acf1-f0d64db2bf24
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetRange method [DirectShow], GetRange method [DirectShow], IAMVideoProcAmp interface, GetRange,IAMVideoProcAmp.GetRange, IAMVideoProcAmp, IAMVideoProcAmp interface [DirectShow], GetRange method, IAMVideoProcAmp::GetRange, IAMVideoProcAmpGetRange, dshow.iamvideoprocamp_getrange, strmif/IAMVideoProcAmp::GetRange
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
-	IAMVideoProcAmp.GetRange
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMVideoProcAmp::GetRange method


## -description



The <code>GetRange</code> method gets the range and default value of a specified video property.




## -parameters




### -param Property [in]

Specifies the property to query, as a value from the <a href="https://msdn.microsoft.com/113e3896-4920-41a3-9ce2-a26c34af4896">VideoProcAmpProperty</a> enumeration.


### -param pMin [out]

Receives the minimum value of the property.
          


### -param pMax [out]

Receives the maximum value of the property.
          


### -param pSteppingDelta [out]

Receives the step size for the property. The step size is the smallest increment by which the property can change.
          


### -param pDefault [out]

Receives the default value of the property.
          


### -param pCapsFlags [out]

Receives a member of the <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a> enumeration, indicating whether the property is controlled automatically or manually.
          


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




<a href="https://msdn.microsoft.com/f789db78-292e-4092-a5dc-1906845fb1dd">Configure the Video Quality</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/28c45790-2e5a-4acb-8a53-93f19c51dc6a">IAMVideoProcAmp Interface</a>
 

 

