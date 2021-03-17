---
UID: NF:ctffunc.ITfFnGetPreferredTouchKeyboardLayout.GetLayout
title: ITfFnGetPreferredTouchKeyboardLayout::GetLayout (ctffunc.h)
description: Obtains the touch keyboard layout identifier of the layout that the IME directs the touch keyboard to show while the IME is active.
helpviewer_keywords: ["GetLayout","GetLayout method [Text Services Framework]","GetLayout method [Text Services Framework]","ITfFnGetPreferredTouchKeyboardLayout interface","ITfFnGetPreferredTouchKeyboardLayout interface [Text Services Framework]","GetLayout method","ITfFnGetPreferredTouchKeyboardLayout.GetLayout","ITfFnGetPreferredTouchKeyboardLayout::GetLayout","ctffunc/ITfFnGetPreferredTouchKeyboardLayout::GetLayout","tsf.itffngetpreferredtouchkeyboardlayout_getlayout"]
old-location: tsf\itffngetpreferredtouchkeyboardlayout_getlayout.htm
tech.root: TSF
ms.assetid: 03C14744-A4A3-4C62-8E7F-CDCC638BBCA1
ms.date: 12/05/2018
ms.keywords: GetLayout, GetLayout method [Text Services Framework], GetLayout method [Text Services Framework],ITfFnGetPreferredTouchKeyboardLayout interface, ITfFnGetPreferredTouchKeyboardLayout interface [Text Services Framework],GetLayout method, ITfFnGetPreferredTouchKeyboardLayout.GetLayout, ITfFnGetPreferredTouchKeyboardLayout::GetLayout, ctffunc/ITfFnGetPreferredTouchKeyboardLayout::GetLayout, tsf.itffngetpreferredtouchkeyboardlayout_getlayout
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfFnGetPreferredTouchKeyboardLayout::GetLayout
 - ctffunc/ITfFnGetPreferredTouchKeyboardLayout::GetLayout
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ctffunc.h
api_name:
 - ITfFnGetPreferredTouchKeyboardLayout.GetLayout
---

# ITfFnGetPreferredTouchKeyboardLayout::GetLayout


## -description

Obtains the touch keyboard layout identifier of the layout that the IME directs the touch keyboard to show while the IME is active.

## -parameters

### -param pTKBLayoutType [out]

Pointer to a <a href="/windows/win32/api/ctffunc/ne-ctffunc-tkblayouttype">TKBLayoutType</a> enumeration that receives the layout type.

### -param pwPreferredLayoutId [out]

Pointer to a <b>WORD</b> value that receives the layout identifier.

## -returns

The touch keyboard always expects S_OK.

## -remarks

<a href="/windows/win32/api/ctffunc/ne-ctffunc-tkblayouttype">TKBLayoutType</a> is an enumeration with the following values.

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

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffngetpreferredtouchkeyboardlayout">ITfFnGetPreferredTouchKeyboardLayout</a>