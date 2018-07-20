---
UID: NF:strmif.IDvdState.GetParentalLevel
title: IDvdState::GetParentalLevel
author: windows-sdk-content
description: The GetParentalLevel method retrieves the user's parental level as saved in the DvdState object.
old-location: dshow\idvdstate_getparentallevel.htm
old-project: DirectShow
ms.assetid: f87c128f-d751-4593-ac26-3249b803bbe4
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetParentalLevel, GetParentalLevel method [DirectShow], GetParentalLevel method [DirectShow],IDvdState interface, IDvdState interface [DirectShow],GetParentalLevel method, IDvdState.GetParentalLevel, IDvdState::GetParentalLevel, IDvdStateGetParentalLevel, dshow.idvdstate_getparentallevel, strmif/IDvdState::GetParentalLevel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IDvdState.GetParentalLevel
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdState::GetParentalLevel


## -description



The <code>GetParentalLevel</code> method retrieves the user's parental level as saved in the <b>DvdState</b> object.




## -parameters




### -param pulParentalLevel [out]

Receives the parental level.


## -returns



Returns one of the following values.

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
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/df30a3b9-7541-42a8-b642-3b6450a0345e">IDvdState Interface</a>
 

 

