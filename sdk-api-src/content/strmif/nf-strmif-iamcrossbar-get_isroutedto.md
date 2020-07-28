---
UID: NF:strmif.IAMCrossbar.get_IsRoutedTo
title: IAMCrossbar::get_IsRoutedTo (strmif.h)
description: The get_IsRoutedTo method retrieves the input pin that is currently routed to the specified output pin.
helpviewer_keywords: ["IAMCrossbar interface [DirectShow]","get_IsRoutedTo method","IAMCrossbar.get_IsRoutedTo","IAMCrossbar::get_IsRoutedTo","IAMCrossbarget_IsRoutedTo","dshow.iamcrossbar_get_isroutedto","get_IsRoutedTo","get_IsRoutedTo method [DirectShow]","get_IsRoutedTo method [DirectShow]","IAMCrossbar interface","strmif/IAMCrossbar::get_IsRoutedTo"]
old-location: dshow\iamcrossbar_get_isroutedto.htm
tech.root: dshow
ms.assetid: fbd59205-ef0a-4e1c-b9d3-63a083c0a7f6
ms.date: 12/05/2018
ms.keywords: IAMCrossbar interface [DirectShow],get_IsRoutedTo method, IAMCrossbar.get_IsRoutedTo, IAMCrossbar::get_IsRoutedTo, IAMCrossbarget_IsRoutedTo, dshow.iamcrossbar_get_isroutedto, get_IsRoutedTo, get_IsRoutedTo method [DirectShow], get_IsRoutedTo method [DirectShow],IAMCrossbar interface, strmif/IAMCrossbar::get_IsRoutedTo
f1_keywords:
- strmif/IAMCrossbar.get_IsRoutedTo
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
- IAMCrossbar.get_IsRoutedTo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMCrossbar::get_IsRoutedTo


## -description



The <code>get_IsRoutedTo</code> method retrieves the input pin that is currently routed to the specified output pin.




## -parameters




### -param OutputPinIndex [in]

Specifies the index of the output pin.


### -param InputPinIndex [out]

Pointer to a variable that receives the index of the input pin, or -1 if no input pin is routed to this output pin.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No input pin is routed to this output pin.

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



Output pins and input pins are both indexed from zero. To determine the number of output and input pins, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamcrossbar-get_pincounts">IAMCrossbar::get_PinCounts</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamcrossbar">IAMCrossbar Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/working-with-crossbars">Working with Crossbars</a>
 

 

