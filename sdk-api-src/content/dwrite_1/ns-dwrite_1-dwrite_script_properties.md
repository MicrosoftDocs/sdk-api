---
UID: NS:dwrite_1.DWRITE_SCRIPT_PROPERTIES
title: DWRITE_SCRIPT_PROPERTIES (dwrite_1.h)
description: The DWRITE_SCRIPT_PROPERTIES structure specifies script properties for caret navigation and justification.
helpviewer_keywords: ["DWRITE_SCRIPT_PROPERTIES","DWRITE_SCRIPT_PROPERTIES structure [Direct Write]","directwrite.dwrite_script_properties","dwrite_1/DWRITE_SCRIPT_PROPERTIES"]
old-location: directwrite\dwrite_script_properties.htm
tech.root: DirectWrite
ms.assetid: 5210C04E-618B-4FE9-A6FC-6F0FF17A64D5
ms.date: 12/05/2018
ms.keywords: DWRITE_SCRIPT_PROPERTIES, DWRITE_SCRIPT_PROPERTIES structure [Direct Write], directwrite.dwrite_script_properties, dwrite_1/DWRITE_SCRIPT_PROPERTIES
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - DWRITE_SCRIPT_PROPERTIES
 - dwrite_1/DWRITE_SCRIPT_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwrite_1.h
api_name:
 - DWRITE_SCRIPT_PROPERTIES
---

# DWRITE_SCRIPT_PROPERTIES structure


## -description

The <b>DWRITE_SCRIPT_PROPERTIES</b> structure specifies script properties for caret navigation and justification.

## -struct-fields

### -field isoScriptCode

The standardized four character code for the given script. 

<div class="alert"><b>Note</b>  These only include the general Unicode scripts, not any additional <a href="http://unicode.org/iso15924/iso15924-codes.html">ISO 15924</a> scripts for bibliographic distinction.</div>
<div> </div>

### -field isoScriptNumber

The standardized numeric code, ranging 0-999.

### -field clusterLookahead

Number of characters to estimate look-ahead for complex scripts. Latin and all Kana are generally 1. Indic scripts are up to 15, and most others are 8.

<div class="alert"><b>Note</b>  Combining marks and variation selectors can produce clusters that are longer than these look-aheads, so this estimate is considered typical language use. Diacritics must be tested explicitly separately.</div>
<div> </div>

### -field justificationCharacter

Appropriate character to elongate the given script for justification. For example:

<ul>
<li>Arabic    - U+0640 Tatweel</li>
<li>Ogham     - U+1680 Ogham Space Mark</li>
</ul>

### -field restrictCaretToClusters

Restrict the caret to whole clusters, like Thai and Devanagari. Scripts such as Arabic by default allow navigation between clusters. Others like Thai always navigate across whole clusters.

### -field usesWordDividers

The language uses dividers between words, such as spaces between Latin or the Ethiopic wordspace. Examples include Latin, Greek, Devanagari, and Ethiopic. Chinese, Korean, and Thai are excluded.

### -field isDiscreteWriting

The characters are discrete units from each other. This includes both block scripts and clustered scripts. Examples include Latin, Greek, Cyrillic, Hebrew, Chinese, and Thai.

### -field isBlockWriting

The language is a block script, expanding between characters. Examples include Chinese, Japanese, Korean, and Bopomofo.

### -field isDistributedWithinCluster

The language is justified within glyph clusters, not just between glyph clusters, such as the character sequence of Thai Lu and Sara Am (U+E026, U+E033), which form a single cluster but still expand between them. Examples include Thai, Lao, and Khmer.

### -field isConnectedWriting

The script's clusters are connected to each other (such as the baseline-linked Devanagari), and no separation is added between characters.

<div class="alert"><b>Note</b>  Cursively linked scripts like Arabic are also connected (but not all connected scripts are cursive). </div>
<div> </div>
Examples include Devanagari, Arabic, Syriac, Bengala, Gurmukhi, and Ogham. Latin, Chinese, and Thaana are excluded.

### -field isCursiveWriting

The script is naturally cursive (Arabic and Syriac), meaning it uses other justification methods like kashida extension rather than inter-character spacing.

<div class="alert"><b>Note</b>   Although other scripts like Latin and Japanese might actually support handwritten cursive forms, they are not considered cursive scripts.</div>
<div> </div>
Examples include Arabic, Syriac, and Mongolian. Thaana, Devanagari, Latin, and Chinese are excluded.

### -field reserved

Reserved

## -see-also

<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties">IDWriteTextAnalyzer1::GetScriptProperties</a>

