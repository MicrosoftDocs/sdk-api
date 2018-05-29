---
UID: NF:strmif.IDvdInfo2.GetCurrentButton
title: IDvdInfo2::GetCurrentButton
author: windows-sdk-content
description: The GetCurrentButton method retrieves the number of available buttons and the number of the currently selected button.
old-location: dshow\idvdinfo2_getcurrentbutton.htm
old-project: DirectShow
ms.assetid: 9e8d8a0e-6db8-495b-b968-8a4e63435b99
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetCurrentButton, GetCurrentButton method [DirectShow], GetCurrentButton method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetCurrentButton method, IDvdInfo2.GetCurrentButton, IDvdInfo2::GetCurrentButton, IDvdInfo2GetCurrentButton, dshow.idvdinfo2_getcurrentbutton, strmif/IDvdInfo2::GetCurrentButton
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
-	IDvdInfo2.GetCurrentButton
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo2::GetCurrentButton


## -description



The <code>GetCurrentButton</code> method retrieves the number of available buttons and the number of the currently selected button.




## -parameters




### -param pulButtonsAvailable [out]

Receives the number of buttons available.


### -param pulCurrentButton [out]

Receives the number (from 1 through 36) of the currently selected button.


## -returns



Returns one of the following <b>HRESULT</b> values.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the pointer arguments is not valid.

</td>
</tr>
</table>
 




## -remarks



If buttons are not present, both <i>pulButtonsAvailable</i> and <i>pulCurrentButton</i> are set to zero.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/af6c841d-ca06-4535-b418-14409fa78c81">EC_DVD_BUTTON_CHANGE</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

