---
UID: NF:mpconfig.IMixerPinConfig.GetBlendingParameter
title: IMixerPinConfig::GetBlendingParameter (mpconfig.h)
author: windows-sdk-content
description: The GetBlendingParameter method retrieves the value of the blending parameter that defines how a secondary stream is blended with a primary stream.
old-location: dshow\imixerpinconfig_getblendingparameter.htm
tech.root: DirectShow
ms.assetid: bcd54b8d-d742-4ac0-bcea-8de77b7f0074
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetBlendingParameter, GetBlendingParameter method [DirectShow], GetBlendingParameter method [DirectShow],IMixerPinConfig interface, IMixerPinConfig interface [DirectShow],GetBlendingParameter method, IMixerPinConfig.GetBlendingParameter, IMixerPinConfig::GetBlendingParameter, IMixerPinConfigGetBlendingParameter, dshow.imixerpinconfig_getblendingparameter, mpconfig/IMixerPinConfig::GetBlendingParameter
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
 - IMixerPinConfig.GetBlendingParameter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMixerPinConfig::GetBlendingParameter


## -description



The <code>GetBlendingParameter</code> method retrieves the value of the blending parameter that defines how a secondary stream is blended with a primary stream.




## -parameters




### -param pdwBlendingParameter [out]

Pointer to a value between 0 and 255 that indicates the amount of blending between a primary stream and a secondary stream.


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
Value outside of possible range (0-255).

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



A value of zero indicates that the secondary stream is invisible; a value of 255 indicates the primary stream is invisible in the area that the secondary stream occupies.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a4f3462-4596-4f02-a41f-47161f8aa4db">IMixerPinConfig Interface</a>



<a href="https://msdn.microsoft.com/262814eb-386b-409e-b22c-48f9f2a845b4">IMixerPinConfig::SetBlendingParameter</a>
 

 

