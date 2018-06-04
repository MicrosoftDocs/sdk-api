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

# ITfFnGetPreferredTouchKeyboardLayout::GetLayout


## -description


Obtains the touch keyboard layout identifier of the layout that the IME directs the touch keyboard to show while the IME is active.


## -parameters




### -param pTKBLayoutType [out]

Pointer to a <a href="https://msdn.microsoft.com/65C46775-9D4D-4C80-A5F0-6713C805053D">TKBLayoutType</a> enumeration that receives the layout type.


### -param pwPreferredLayoutId [out]

Pointer to a <b>WORD</b> value that receives the layout identifier.


## -returns



The touch keyboard always expects S_OK.




## -remarks




<a href="https://msdn.microsoft.com/65C46775-9D4D-4C80-A5F0-6713C805053D">TKBLayoutType</a> is an enumeration with the following values.

<table>
<tr>
<td>TKBLT_UNDEFINED</td>
<td>Undefined.</td>
</tr>
<tr>
<td>TKBLT_CLASSIC</td>
<td>
The touch keyboard is to use a classic layout.

Classic layouts represent the legacy layouts of physical keyboards.

</td>
</tr>
<tr>
<td>TKBLT_OPTIMIZED</td>
<td>
The touch keyboard is to use a touch-optimized layout.

Touch-optimized layouts have been specifically designed with touch in mind.

</td>
</tr>
</table>
 

The layout identifiers returned by this API must be one from the following list.
Each identifier is specific to a certain language, and these are all specific to the touch keyboard.
There is no way to request support for other layouts, or to add new touch optimized layouts dynamically.

<table>
<tr>
<th>Layout Definition                                                                                    </th>
<th>Value</th>
<th>Supported Input Language</th>
</tr>
<tr>
<td>TKBL_UNDEFINED</td>
<td>0</td>
<td>n/a</td>
</tr>
<tr>
<td>TKBL_CLASSIC_TRADITIONAL_CHINESE_PHONETIC</td>
<td>0x0404</td>
<td>CHT</td>
</tr>
<tr>
<td>TKBL_CLASSIC_TRADITIONAL_CHINESE_CHANGJIE</td>
<td>0xF042</td>
<td>CHT</td>
</tr>
<tr>
<td>TKBL_CLASSIC_TRADITIONAL_CHINESE_DAYI</td>
<td>0xF043</td>
<td>CHT</td>
</tr>
<tr>
<td>TKBL_OPT_JAPANESE_ABC</td>
<td>0x0411</td>
<td>JPN</td>
</tr>
<tr>
<td>TKBL_OPT_KOREAN_HANGUL_2_BULSIK</td>
<td>0x0412</td>
<td>KOR</td>
</tr>
<tr>
<td>TKBL_OPT_SIMPLIFIED_CHINESE_PINYIN</td>
<td>0x0804</td>
<td>CHS</td>
</tr>
<tr>
<td>TKBL_OPT_TRADITIONAL_CHINESE_PHONETIC</td>
<td>0x0404</td>
<td>CHT</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1BC4A446-AEDC-44AA-9BD7-786917AD2556">ITfFnGetPreferredTouchKeyboardLayout</a>
 

 

