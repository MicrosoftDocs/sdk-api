---
UID: NS:usp10.tag_SCRIPT_STATE
title: tag_SCRIPT_STATE
author: windows-driver-content
description: Contains script state information.
old-location: intl\script_state.htm
old-project: Intl
ms.assetid: 4b1724f7-7773-42c0-9c19-fbded5aef14e
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: FALSE, SCRIPT_STATE, SCRIPT_STATE structure [Internationalization for Windows Applications], TRUE, _win32_SCRIPT_STATE_str, intl.script_state, tag_SCRIPT_STATE, usp10/SCRIPT_STATE
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SCRIPT_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Usp10.h
api_name:
-	SCRIPT_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# tag_SCRIPT_STATE structure


## -description



Contains script state information.




## -struct-fields




### -field uBidiLevel

Embedding level associated with all characters in the associated run according to the Unicode bidirectional algorithm. When the application passes this structure to <a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a>, this member should be initialized to 0 for a left-to-right base embedding level, or to 1 for a right-to-left base embedding level.


### -field fOverrideDirection

Initial override direction value indicating if the script uses an override level (LRO or RLO code in the string). Possible values are defined in the following table. For an override level, characters are laid out in one direction only, either left to right or right to left. No reordering of digits or strong characters of opposing direction takes place. Note that this value is reset by LRE, RLE, LRO or RLO codes in the string.

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
Use an override level that reflects the embedding level.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Do not use an override level that reflects the embedding level.

</td>
</tr>
</table>
 


### -field fInhibitSymSwap

Value indicating if the shaping engine bypasses mirroring of Unicode mirrored glyphs, for example, brackets. Possible values are defined in the following table. This member is set by Unicode character ISS, and cleared by ASS.

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
Bypass mirroring of Unicode mirrored glyphs.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Do not bypass mirroring of Unicode mirrored glyphs.

</td>
</tr>
</table>
 


### -field fCharShape

Not implemented. Value indicating if character codes in the Arabic Presentation Forms areas of Unicode should be shaped. Possible values are defined in the following table.

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
Shape character codes in the Arabic Presentation Forms areas of Unicode.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Do not shape character codes in the Arabic Presentation Forms areas of Unicode.

</td>
</tr>
</table>
 


### -field fDigitSubstitute

This member provides the same control over digit substitution behavior that might have been obtained in legacy implementations using the now-deprecated Unicode characters U+206E NATIONAL DIGIT SHAPES ("NADS") and U+206F NOMINAL DIGIT SHAPES ("NODS"). Possible values are defined in the following table.

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
Character codes U+0030 through U+0039 are substituted by national digits. 

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Character codes U+0030 through U+0039 are  not substituted by national digits. 

</td>
</tr>
</table>
 


### -field fInhibitLigate

Value indicating if ligatures are used in the shaping of Arabic or Hebrew characters. Possible values are defined in the following table. 

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
Do not use ligatures in the shaping of Arabic or Hebrew characters.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Use ligatures in the shaping of Arabic or Hebrew characters.

</td>
</tr>
</table>
 


### -field fDisplayZWG

Value indicating if nondisplayable control characters are shaped as representational glyphs for languages that need reordering or different glyph shapes, depending on the positions of the characters within a word. Possible values are defined in the following table. Typically, the characters are not displayed. They are shaped to the blank glyph and given a width of 0.
	 

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
Shape control characters as representational glyphs. 

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Do not shape control characters as representational glyphs. 

</td>
</tr>
</table>
 


### -field fArabicNumContext

Value indicating if prior strong characters are Arabic for the purposes of rule P0, as discussed in the Unicode Standard, version 2.0. Possible values are defined in the following table. This member should normally be set to <b>TRUE</b> before itemization of a right-to-left paragraph in an Arabic language, and to <b>FALSE</b> otherwise.

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
Consider prior strong characters to be Arabic for the purposes of rule P0.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Do not consider prior strong characters to be Arabic for the purposes of rule P0.

</td>
</tr>
</table>
 


### -field fGcpClusters

For <a href="https://msdn.microsoft.com/80d3f4b3-503b-4abb-826c-e5c09972ba2f">GetCharacterPlacement</a> legacy support only. Value indicating how <a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a> should generate the array indicated by <i>pwLogClust</i>. Possible values are defined in the following table. This member affects only Arabic and Hebrew items.

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
Generate the array the same way as <a href="https://msdn.microsoft.com/80d3f4b3-503b-4abb-826c-e5c09972ba2f">GetCharacterPlacement</a> does.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Do not generate the array the same way as <a href="https://msdn.microsoft.com/80d3f4b3-503b-4abb-826c-e5c09972ba2f">GetCharacterPlacement</a> does.

</td>
</tr>
</table>
 


### -field fReserved

Reserved; always initialize to 0.


### -field fEngineReserved

Reserved; always initialize to 0.


## -remarks



This structure is used to initialize the Unicode algorithm state as an input to <a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a>. It is also used as a component of the analysis retrieved by <b>ScriptItemize</b>.




## -see-also




<a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a>



<a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/243438fd-5bb2-4b2a-8b33-803029085adb">Uniscribe Structures</a>
 

 

