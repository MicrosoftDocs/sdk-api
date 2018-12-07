---
UID: NF:dwrite.IDWriteTextFormat.SetTextAlignment
title: IDWriteTextFormat::SetTextAlignment
author: windows-sdk-content
description: Sets the alignment of text in a paragraph, relative to the leading and trailing edge of a layout box for a IDWriteTextFormat interface.
old-location: directwrite\IDWriteTextFormat_SetTextAlignment.htm
tech.root: DirectWrite
ms.assetid: 2e7554e3-4e0c-45b1-a874-a3054b0e91dc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteTextFormat interface [Direct Write],SetTextAlignment method, IDWriteTextFormat.SetTextAlignment, IDWriteTextFormat::SetTextAlignment, SetTextAlignment, SetTextAlignment method [Direct Write], SetTextAlignment method [Direct Write],IDWriteTextFormat interface, directwrite.IDWriteTextFormat_SetTextAlignment, dwrite/IDWriteTextFormat::SetTextAlignment
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextFormat.SetTextAlignment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextFormat::SetTextAlignment


## -description


Sets the alignment of text in a paragraph, relative to the leading and trailing edge of a layout box for a <a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a> interface.


## -parameters




### -param textAlignment

Type: <b><a href="https://msdn.microsoft.com/76b347f8-185b-4da6-9647-4d066334ac12">DWRITE_TEXT_ALIGNMENT</a></b>

The text alignment option being set for the paragraph of type DWRITE_TEXT_ALIGNMENT.  For more information, see Remarks.
				  


## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The textAlignment argument is invalid.

</td>
</tr>
</table>
 




## -remarks



The text can be aligned to the leading or trailing edge of the layout box, or it can be centered.  The following illustration shows text with the alignment set to <a href="https://msdn.microsoft.com/76b347f8-185b-4da6-9647-4d066334ac12">DWRITE_TEXT_ALIGNMENT_LEADING</a>, <b>DWRITE_TEXT_ALIGNMENT_CENTER</b>, and <b>DWRITE_TEXT_ALIGNMENT_TRAILING</b>, respectively.  

<img alt="Illustration of text paragraphs with leading, centered, and trailing alignment" src="./images/TextAlignment.png"/>

<div class="alert"><b>Note</b>  The alignment is dependent on reading direction, the above is for left-to-right reading direction.  For right-to-left reading direction it would be the opposite.</div>
<div> </div>
See <a href="https://msdn.microsoft.com/76b347f8-185b-4da6-9647-4d066334ac12">DWRITE_TEXT_ALIGNMENT</a> for more information.
			


#### Examples


```cpp
if (SUCCEEDED(hr))
{
    hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
}

```





## -see-also




<a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a>
 

 

