---
UID: NF:mpconfig.IMixerPinConfig.SetBlendingParameter
title: IMixerPinConfig::SetBlendingParameter
author: windows-sdk-content
description: The SetBlendingParameter method sets the blending parameter that defines how a secondary stream is blended with a primary stream.
old-location: dshow\imixerpinconfig_setblendingparameter.htm
old-project: DirectShow
ms.assetid: 262814eb-386b-409e-b22c-48f9f2a845b4
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IMixerPinConfig interface [DirectShow],SetBlendingParameter method, IMixerPinConfig.SetBlendingParameter, IMixerPinConfig::SetBlendingParameter, IMixerPinConfigSetBlendingParameter, SetBlendingParameter, SetBlendingParameter method [DirectShow], SetBlendingParameter method [DirectShow],IMixerPinConfig interface, dshow.imixerpinconfig_setblendingparameter, mpconfig/IMixerPinConfig::SetBlendingParameter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mpconfig.h
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
req.typenames: AM_ASPECT_RATIO_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMixerPinConfig.SetBlendingParameter
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMixerPinConfig::SetBlendingParameter


## -description



The <code>SetBlendingParameter</code> method sets the blending parameter that defines how a secondary stream is blended with a primary stream.




## -parameters




### -param dwBlendingParameter [in]

Value between 0 and 255 that indicates the amount of blending between a primary stream and a secondary stream.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Method called on primary stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Value outside of possible range (0 to 255).

</td>
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
</table>
 




## -remarks



The value of the <i>dwBlendingParameter</i> parameter must be between 0 and 255, where 0 makes the secondary stream invisible and 255 makes the primary stream invisible in the area that the secondary stream occupies. If no value is set the default is 255.

This method is not intended to be called on the primary stream.

<div class="alert"><b>Note</b>  Current DirectShow implementation of this interface allows only values of 0 or 255 for the <i>dwBlendingParameter</i> parameter. Any other values are invalid.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a4f3462-4596-4f02-a41f-47161f8aa4db">IMixerPinConfig Interface</a>



<a href="https://msdn.microsoft.com/bcd54b8d-d742-4ac0-bcea-8de77b7f0074">IMixerPinConfig::GetBlendingParameter</a>
 

 

