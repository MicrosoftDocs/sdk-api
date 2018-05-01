---
UID: NF:strmif.IAMCrossbar.get_PinCounts
title: IAMCrossbar::get_PinCounts method
author: windows-driver-content
description: The get_PinCounts method retrieves the number of input and output pins on the crossbar filter.
old-location: dshow\iamcrossbar_get_pincounts.htm
old-project: DirectShow
ms.assetid: 66ea86a6-82c3-4f91-a2d3-a08014f555be
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IAMCrossbar, IAMCrossbar interface [DirectShow], get_PinCounts method, IAMCrossbar::get_PinCounts, IAMCrossbarget_PinCounts, dshow.iamcrossbar_get_pincounts, get_PinCounts method [DirectShow], get_PinCounts method [DirectShow], IAMCrossbar interface, get_PinCounts,IAMCrossbar.get_PinCounts, strmif/IAMCrossbar::get_PinCounts
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
-	IAMCrossbar.get_PinCounts
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMCrossbar::get_PinCounts method


## -description



The <code>get_PinCounts</code> method retrieves the number of input and output pins on the crossbar filter.




## -parameters




### -param OutputPinCount [out]

Pointer to variable that receives the number of output pins.


### -param InputPinCount [out]

Pointer to variable that receives the number of input pins.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



The other <a href="https://msdn.microsoft.com/9eef4923-62e7-475e-85e6-de8c1eefe483">IAMCrossbar</a> methods take parameters that specify pins by index number. For these methods, output pins and input pins are both indexed from zero. Use the <code>get_PinCounts</code> method to determine the upper bounds for each.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9eef4923-62e7-475e-85e6-de8c1eefe483">IAMCrossbar Interface</a>



<a href="https://msdn.microsoft.com/6e8ee9c3-6776-498b-ad38-36f8172a27ae">Working with Crossbars</a>
 

 

