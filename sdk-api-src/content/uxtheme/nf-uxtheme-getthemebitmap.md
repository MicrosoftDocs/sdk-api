---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# GetThemeBitmap function


## -description


Retrieves the bitmap associated with a particular theme, part, state, and property.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

A handle to theme data.


### -param iPartId [in]

Type: <b>int</b>

The part that contains the bitmap. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

The state of the part.


### -param iPropId [in]

Type: <b>int</b>

The property to retrieve. Pass zero to automatically select the first available bitmap for this part and state, 
                or use one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TMT_DIBDATA"></a><a id="tmt_dibdata"></a><dl>
<dt><b>TMT_DIBDATA</b></dt>
</dl>
</td>
<td width="60%">
The background image.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_GLYPHDIBDATA"></a><a id="tmt_glyphdibdata"></a><dl>
<dt><b>TMT_GLYPHDIBDATA</b></dt>
</dl>
</td>
<td width="60%">
The glyph image drawn on top of the background, if present. 

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_HBITMAP"></a><a id="tmt_hbitmap"></a><dl>
<dt><b>TMT_HBITMAP</b></dt>
</dl>
</td>
<td width="60%">
Not currently supported.

</td>
</tr>
</table>
 


### -param dwFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG</a></b>

The flags that specify how the bitmap is to be retrieved. Can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GBF_DIRECT"></a><a id="gbf_direct"></a><dl>
<dt><b>GBF_DIRECT</b></dt>
</dl>
</td>
<td width="60%">
Retrieves a handle to the existing bitmap.

</td>
</tr>
<tr>
<td width="40%"><a id="GBF_COPY"></a><a id="gbf_copy"></a><dl>
<dt><b>GBF_COPY</b></dt>
</dl>
</td>
<td width="60%">
Retrieves a copy of the bitmap.

</td>
</tr>
<tr>
<td width="40%"><a id="GBF_VALIDBITS"></a><a id="gbf_validbits"></a><dl>
<dt><b>GBF_VALIDBITS</b></dt>
</dl>
</td>
<td width="60%">
<b>GBF_DIRECT</b> | <b>GBF_COPY</b>

</td>
</tr>
</table>
 


### -param phBitmap [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HBITMAP</a>*</b>

A pointer that receives a handle to the requested bitmap.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <i>dwFlags</i> is set to <b>GBF_COPY</b>, release the bitmap stored in <i>phBitmap</i> when no longer needed by calling <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>.



