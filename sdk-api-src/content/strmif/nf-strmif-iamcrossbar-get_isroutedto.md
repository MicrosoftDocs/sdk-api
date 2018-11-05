---
UID: NF:strmif.IAMCrossbar.get_IsRoutedTo
title: IAMCrossbar::get_IsRoutedTo
author: windows-sdk-content
description: The get_IsRoutedTo method retrieves the input pin that is currently routed to the specified output pin.
old-location: dshow\iamcrossbar_get_isroutedto.htm
tech.root: DirectShow
ms.assetid: fbd59205-ef0a-4e1c-b9d3-63a083c0a7f6
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAMCrossbar interface [DirectShow],get_IsRoutedTo method, IAMCrossbar.get_IsRoutedTo, IAMCrossbar::get_IsRoutedTo, IAMCrossbarget_IsRoutedTo, dshow.iamcrossbar_get_isroutedto, get_IsRoutedTo, get_IsRoutedTo method [DirectShow], get_IsRoutedTo method [DirectShow],IAMCrossbar interface, strmif/IAMCrossbar::get_IsRoutedTo
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



Output pins and input pins are both indexed from zero. To determine the number of output and input pins, call the <a href="https://msdn.microsoft.com/66ea86a6-82c3-4f91-a2d3-a08014f555be">IAMCrossbar::get_PinCounts</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9eef4923-62e7-475e-85e6-de8c1eefe483">IAMCrossbar Interface</a>



<a href="https://msdn.microsoft.com/6e8ee9c3-6776-498b-ad38-36f8172a27ae">Working with Crossbars</a>
 

 

