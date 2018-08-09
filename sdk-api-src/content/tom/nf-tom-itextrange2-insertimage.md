---
UID: NF:tom.ITextRange2.InsertImage
title: ITextRange2::InsertImage
author: windows-sdk-content
description: Inserts an image into this range.
old-location: controls\itextrange2_insertimage.htm
old-project: controls
ms.assetid: CBC71EDC-CBE3-4C44-84C8-6AE6DEBC8D0C
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextRange2 interface [Windows Controls],InsertImage method, ITextRange2.InsertImage, ITextRange2::InsertImage, InsertImage, InsertImage method [Windows Controls], InsertImage method [Windows Controls],ITextRange2 interface, TA_BASELINE, TA_BOTTOM, TA_TOP, controls.itextrange2_insertimage, tom/ITextRange2::InsertImage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange2.InsertImage
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange2::InsertImage


## -description


Inserts an image into this range.


## -parameters




### -param width [in]

Type: <b>long</b>

The width, in HIMETRIC units (0.01 mm), of the image.


### -param height [in]

Type: <b>long</b>

The height, in HIMETRIC units, of the image.


### -param ascent [in]

Type: <b>long</b>

If <i>Type</i> is TA_BASELINE, this parameter is the distance, in HIMETRIC units, that the top of the image extends above the text baseline. If <i>Type</i> is TA_BASELINE and <i>ascent</i> is zero, the bottom of the image is placed at the text baseline.


### -param Type [in]

Type: <b>long</b>

The vertical alignment of the image. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TA_BASELINE"></a><a id="ta_baseline"></a><dl>
<dt><b>TA_BASELINE</b></dt>
</dl>
</td>
<td width="60%">
Align the image relative to the text baseline. 

</td>
</tr>
<tr>
<td width="40%"><a id="TA_BOTTOM"></a><a id="ta_bottom"></a><dl>
<dt><b>TA_BOTTOM</b></dt>
</dl>
</td>
<td width="60%">
Align the bottom of the image at the bottom of the text line. 

</td>
</tr>
<tr>
<td width="40%"><a id="TA_TOP"></a><a id="ta_top"></a><dl>
<dt><b>TA_TOP</b></dt>
</dl>
</td>
<td width="60%">
Align the top of the image at the top of the text line

</td>
</tr>
</table>
 


### -param bstrAltText [in]

Type: <b><a href="https://msdn.microsoft.com/1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>

The alternate text for the image.


### -param pStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a></b>

The stream that contains the image data. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the range is nondegenerate, the image replaces the text in the range. 




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>
 

 

