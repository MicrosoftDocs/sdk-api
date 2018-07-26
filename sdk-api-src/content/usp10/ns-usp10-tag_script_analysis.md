---
UID: NS:usp10.tag_SCRIPT_ANALYSIS
title: tag_SCRIPT_ANALYSIS
author: windows-sdk-content
description: Contains a portion of a Unicode string, that is, an &#0034;item&#0034;.
old-location: intl\script_analysis.htm
old-project: Intl
ms.assetid: c673d5cc-c4ca-4238-8090-55abe3db324b
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: FALSE, SCRIPT_ANALYSIS, SCRIPT_ANALYSIS structure [Internationalization for Windows Applications], TRUE, _win32_SCRIPT_ANALYSIS_str, intl.script_analysis, tag_SCRIPT_ANALYSIS, usp10/SCRIPT_ANALYSIS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: usp10.h
req.include-header: 
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
tech.root: 
req.typenames: SCRIPT_ANALYSIS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Usp10.h
api_name:
 - SCRIPT_ANALYSIS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# tag_SCRIPT_ANALYSIS structure


## -description



Contains a portion of a Unicode string, that is, an "item".




## -struct-fields




### -field eScript

Opaque value identifying the engine that Uniscribe uses when calling the <a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a>, <a href="https://msdn.microsoft.com/7f88432f-052f-4781-8346-31c8a0771e51">ScriptPlace</a>, and <a href="https://msdn.microsoft.com/8d69caeb-4c02-4a9f-9dd5-ac3c13561a57">ScriptTextOut</a> functions for the item. The value for this member is undefined and applications should not rely on its value being the same from one release to the next. An application can obtain the attributes of <b>eScript</b> by calling <a href="https://msdn.microsoft.com/4799829d-8122-4bb4-839c-92f177cfd2da">ScriptGetProperties</a>.

To disable shaping, the application should set this member to SCRIPT_UNDEFINED.


### -field fRTL

Value indicating rendering direction. Possible values are defined in the following table. This member is set to <b>TRUE</b> for a number in a left-to-right run, because digits are always displayed left to right, or <b>FALSE</b> for a number in a right-to-left run. The value of this member is normally identical to the parity of the Unicode embedding level, but it might differ if overridden by <a href="https://msdn.microsoft.com/80d3f4b3-503b-4abb-826c-e5c09972ba2f">GetCharacterPlacement</a> legacy support.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
Use a right-to-left rendering direction.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Use a left-to-right rendering direction.

</td>
</tr>
</table>
 


### -field fLayoutRTL

Value indicating layout direction for a number. Possible values are defined in the following table. This member is usually the same as the value assigned to <b>fRTL</b> for a number in a right-to-left run.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
Lay out the number in a right-to-left run, because it is read as part of the right-to-left sequence.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Lay out the number in a left-to-right run, because it is read as part of the left-to-right sequence.

</td>
</tr>
</table>
 


### -field fLinkBefore

Value indicating if the shaping engine shapes the first character of the item as if it joins with a previous character. Possible values are defined in the following table. This member is set by <a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a>. The application can override the value before calling <a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
Shape the first character by linking with a previous character.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Do not shape the first character by linking with a previous character.

</td>
</tr>
</table>
 


### -field fLinkAfter

Value indicating if the shaping engine shapes the last character of the item as if it joins with a subsequent character. Possible values are defined in the following table. This member is set by <a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a>. The application can override the value before calling <b>ScriptItemize</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
Shape the last character by linking with a subsequent character.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Do not shape the last character by linking with a subsequent character.

</td>
</tr>
</table>
 


### -field fLogicalOrder

Value indicating if the shaping engine generates all glyph-related arrays in logical order. Possible values are defined in the following table. This member is set to <b>FALSE</b> by <a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a>. The application can override the value before calling <a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
Generate all glyph-related arrays in logical order.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Generate all glyph-related arrays in visual order, with the first array entry corresponding to the leftmost glyph. This value is the default.

</td>
</tr>
</table>
 


### -field fNoGlyphIndex

Value indicating the use of glyphs for the item. Possible values are defined in the following table. The application can set this member to <b>TRUE</b> on input to <a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a> to disable the use of glyphs for the item. Additionally, <b>ScriptShape</b> sets it to <b>TRUE</b> for a hardware context containing symbolic, unrecognized, and device fonts.

Disabling the use of glyphs also disables complex script shaping. Setting this member to <b>TRUE</b> implements shaping and placing directly by calls to <a href="https://msdn.microsoft.com/b873a059-5aa3-47d0-b109-7acd542c7d79">GetTextExtentExPoint</a> and <a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
Disable the use of glyphs for the item. This value is used for bitmap, vector, and device fonts.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Enable the use of glyphs for the item. This value is the default.

</td>
</tr>
</table>
 


### -field s

A <a href="https://msdn.microsoft.com/4b1724f7-7773-42c0-9c19-fbded5aef14e">SCRIPT_STATE</a> structure containing a copy of the Unicode algorithm state.


## -remarks



This structure is filled by <a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a> or <a href="https://msdn.microsoft.com/da15d6b3-6725-43b8-9a2c-c19269a79d1e">ScriptItemizeOpenType</a>, each of which breaks a Unicode string into individually shapeable items. Neither function accesses the <b>SCRIPT_ANALYSIS</b> structure directly. Each function handles an array of <a href="https://msdn.microsoft.com/d309f3a7-fec3-4999-bbbe-bb85ceecb4c4">SCRIPT_ITEM</a> structures, each of which has a member defining a <b>SCRIPT_ANALYSIS</b> structure.

Applications that use <a href="https://msdn.microsoft.com/da15d6b3-6725-43b8-9a2c-c19269a79d1e">ScriptItemizeOpenType</a> instead of <a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a> should also use <a href="https://msdn.microsoft.com/d2e062a6-2ec8-4057-b525-d1cd719dc736">ScriptShapeOpenType</a> and <a href="https://msdn.microsoft.com/dd456988-ec9d-4e62-a93f-753ac08a18d9">ScriptPlaceOpenType</a> instead of <a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a> and <a href="https://msdn.microsoft.com/7f88432f-052f-4781-8346-31c8a0771e51">ScriptPlace</a>. For more information, see <a href="https://msdn.microsoft.com/e1adc567-0445-4deb-8634-25653f82127c">Displaying Text with Uniscribe</a>.




## -see-also




<a href="https://msdn.microsoft.com/d309f3a7-fec3-4999-bbbe-bb85ceecb4c4">SCRIPT_ITEM</a>



<a href="https://msdn.microsoft.com/4b1724f7-7773-42c0-9c19-fbded5aef14e">SCRIPT_STATE</a>



<a href="https://msdn.microsoft.com/4799829d-8122-4bb4-839c-92f177cfd2da">ScriptGetProperties</a>



<a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a>



<a href="https://msdn.microsoft.com/da15d6b3-6725-43b8-9a2c-c19269a79d1e">ScriptItemizeOpenType</a>



<a href="https://msdn.microsoft.com/7f88432f-052f-4781-8346-31c8a0771e51">ScriptPlace</a>



<a href="https://msdn.microsoft.com/dd456988-ec9d-4e62-a93f-753ac08a18d9">ScriptPlaceOpenType</a>



<a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a>



<a href="https://msdn.microsoft.com/d2e062a6-2ec8-4057-b525-d1cd719dc736">ScriptShapeOpenType</a>



<a href="https://msdn.microsoft.com/8d69caeb-4c02-4a9f-9dd5-ac3c13561a57">ScriptTextOut</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/243438fd-5bb2-4b2a-8b33-803029085adb">Uniscribe Structures</a>
 

 

