---
UID: NF:dwrite.IDWriteTextLayout.SetFontWeight
title: IDWriteTextLayout::SetFontWeight
author: windows-sdk-content
description: Sets the font weight for text within a text range specified by a DWRITE_TEXT_RANGE structure.
old-location: directwrite\IDWriteTextLayout_SetFontWeight.htm
tech.root: DirectWrite
ms.assetid: c6b65548-c486-4006-afe9-95bc628bbf70
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDWriteTextLayout interface [Direct Write],SetFontWeight method, IDWriteTextLayout.SetFontWeight, IDWriteTextLayout::SetFontWeight, SetFontWeight, SetFontWeight method [Direct Write], SetFontWeight method [Direct Write],IDWriteTextLayout interface, directwrite.IDWriteTextLayout_SetFontWeight, dwrite/IDWriteTextLayout::SetFontWeight
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
 - IDWriteTextLayout.SetFontWeight
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::SetFontWeight


## -description


 Sets the font weight for text within a text range specified by a <a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a> structure.


## -parameters




### -param fontWeight

Type: <b><a href="https://msdn.microsoft.com/82396f80-eb62-4865-ba07-9653220c84f2">DWRITE_FONT_WEIGHT</a></b>

The font weight to be set for text within the range specified by <i>textRange</i>.


### -param textRange

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a></b>

Text range to which this change applies.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The font weight can be set to one of the predefined font weight values provided in the <a href="https://msdn.microsoft.com/82396f80-eb62-4865-ba07-9653220c84f2">DWRITE_FONT_WEIGHT</a> enumeration or an integer from 1 to 999.  Values outside this range will cause the method to fail with an <b>E_INVALIDARG</b> return value.

The following illustration shows an example of Normal and UltraBold weights for the Palatino Linotype typeface.

<img alt='Illustration of the letter "W" in Normal and UltraBold weights' src="images/FontWeight_for_Palatino.png"/>

#### Examples

The following code illustrates how to set the font weight to bold.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Set the font weight to bold for the entire string.
DWRITE_TEXT_RANGE textRange = {0, cTextLength_};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_-&gt;SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

