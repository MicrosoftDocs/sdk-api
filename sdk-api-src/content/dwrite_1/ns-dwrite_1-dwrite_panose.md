---
UID: NS:dwrite_1.DWRITE_PANOSE
title: DWRITE_PANOSE
author: windows-sdk-content
description: The DWRITE_PANOSE union describes typeface classification values that you use with IDWriteFont1::GetPanose to select and match the font.
old-location: directwrite\dwrite_panose.htm
old-project: DirectWrite
ms.assetid: B65B4C8E-1CA0-47AC-AA3F-8F2EACC5C11A
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: DWRITE_PANOSE, DWRITE_PANOSE union [Direct Write], directwrite.dwrite_panose, dwrite_1/DWRITE_PANOSE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwrite_1.h
api_name:
 - DWRITE_PANOSE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DWRITE_PANOSE structure


## -description


The <b>DWRITE_PANOSE</b> union describes typeface classification values that you use with <a href="https://msdn.microsoft.com/DD31C1D6-4CD2-4ED0-BF9F-CAF587C613E6">IDWriteFont1::GetPanose</a> to select and match the font.


## -struct-fields




### -field values

 


### -field familyKind

A <a href="https://msdn.microsoft.com/8CC6E653-FF82-4BBA-9DDE-F3F4960C4BBB">DWRITE_PANOSE_FAMILY</a>-typed value that specifies the typeface classification values to get.


### -field text


### -field text.familyKind


			
		    The <a href="https://msdn.microsoft.com/library/Hh995028(v=VS.85).aspx">DWRITE_PANOSE_FAMILY_TEXT_DISPLAY</a> value (2) that specifies text display typeface classification.


### -field text.serifStyle


			
		    A <a href="https://msdn.microsoft.com/F141B81F-7DF2-4E7C-A373-36C7FEF53857">DWRITE_PANOSE_SERIF_STYLE</a>-typed value that specifies the serif style of text.


### -field text.weight


			
		    A <a href="https://msdn.microsoft.com/9309C68B-1193-47EF-A577-9DC0EEE18F4C">DWRITE_PANOSE_WEIGHT</a>-typed value that specifies the weight of the text.


### -field text.proportion

A <a href="https://msdn.microsoft.com/03A43DD4-89D1-4895-B224-9BCC8C34B2E4">DWRITE_PANOSE_PROPORTION</a>-typed value that specifies the proportion for the text.


### -field text.contrast

A <a href="https://msdn.microsoft.com/EB526A2A-1E85-4A65-B485-4AE87F45C2A0">DWRITE_PANOSE_CONTRAST</a>-typed value that specifies the contrast for the text.


### -field text.strokeVariation


			
		    A <a href="https://msdn.microsoft.com/3E30D318-1A88-4563-93D7-7E84893D04CE">DWRITE_PANOSE_STROKE_VARIATION</a>-typed value that specifies the stroke variation for the text.


### -field text.armStyle


			
		    A <a href="https://msdn.microsoft.com/E0DFBE06-C2CF-4E47-A68E-A7D17755B42F">DWRITE_PANOSE_ARM_STYLE</a>-typed value that specifies the arm style of text.


### -field text.letterform


			
		    A <a href="https://msdn.microsoft.com/67E1A497-A7C5-441E-BE51-0598E80BAEB3">DWRITE_PANOSE_LETTERFORM</a>-typed value that specifies the letter form for the text.
			
		    


### -field text.midline


			
		    A <a href="https://msdn.microsoft.com/97639251-7703-4F3B-85FC-E33D666CA837">DWRITE_PANOSE_MIDLINE</a>-typed value that specifies the midline for the text.


### -field text.xHeight


			
		    A <a href="https://msdn.microsoft.com/E4448DC6-9014-41FB-B14B-2C6FB4E4D13D">DWRITE_PANOSE_XHEIGHT</a>-typed value that specifies the relative size of lowercase text.


### -field script


### -field script.familyKind


			
		    The <a href="https://msdn.microsoft.com/library/Hh995028(v=VS.85).aspx">DWRITE_PANOSE_FAMILY_SCRIPT</a> value (3) that specifies script typeface classification.


### -field script.toolKind


			
		    A <a href="https://msdn.microsoft.com/06426D8B-BBAA-4FF3-B5CB-09B72A95414A">DWRITE_PANOSE_TOOL_KIND</a>-typed value that specifies the kind of tool for the script.
			
		    


### -field script.weight


			
		    A <a href="https://msdn.microsoft.com/9309C68B-1193-47EF-A577-9DC0EEE18F4C">DWRITE_PANOSE_WEIGHT</a>-typed value that specifies the weight of the script.


### -field script.spacing


			
		    A <a href="https://msdn.microsoft.com/BA841315-2B57-4B35-A6E4-2343EBE67AC8">DWRITE_PANOSE_SPACING</a>-typed value that specifies the spacing of the script.


### -field script.aspectRatio


			
		    A <a href="https://msdn.microsoft.com/B371DB94-EE4A-4BAC-B61D-F6C4A719E176">DWRITE_PANOSE_ASPECT_RATIO</a>-typed value that specifies the aspect ratio of the script.


### -field script.contrast

A <a href="https://msdn.microsoft.com/EB526A2A-1E85-4A65-B485-4AE87F45C2A0">DWRITE_PANOSE_CONTRAST</a>-typed value that specifies the contrast for the script.


### -field script.scriptTopology


			
		    
			
		    A <a href="https://msdn.microsoft.com/6D546DCF-3812-495C-AAF3-A7C2E14CACA2">DWRITE_PANOSE_SCRIPT_TOPOLOGY</a>-typed value that specifies the script topology.


### -field script.scriptForm

A <a href="https://msdn.microsoft.com/F6F56DEE-F981-40F8-8B35-ABFE7C82EA2C">DWRITE_PANOSE_SCRIPT_FORM</a>-typed value that specifies the script form.
			
		    


### -field script.finials


			
		    A <a href="https://msdn.microsoft.com/8B0B2768-26E6-4163-91DD-DFE69C981C56">DWRITE_PANOSE_FINIALS</a>-typed value that specifies the script finials.


### -field script.xAscent


			
		    A <a href="https://msdn.microsoft.com/CD32DC3D-57C5-4B21-955B-D023D8E3DD36">DWRITE_PANOSE_XASCENT</a>-typed value that specifies the relative size of lowercase letters.


### -field decorative


### -field decorative.familyKind


			
		    The <a href="https://msdn.microsoft.com/library/Hh995028(v=VS.85).aspx">DWRITE_PANOSE_FAMILY_DECORATIVE</a> value (4) that specifies decorative typeface classification.


### -field decorative.decorativeClass


			
		    
			
		    A <a href="https://msdn.microsoft.com/54885610-7749-4012-AB25-8968871CEBCE">DWRITE_PANOSE_DECORATIVE_CLASS</a>-typed value that specifies the class of the decorative typeface.


### -field decorative.weight


			
		    A <a href="https://msdn.microsoft.com/9309C68B-1193-47EF-A577-9DC0EEE18F4C">DWRITE_PANOSE_WEIGHT</a>-typed value that specifies the weight of the decorative typeface.


### -field decorative.aspect

A <a href="https://msdn.microsoft.com/D546354A-3875-43B1-9B16-7691611D1AD9">DWRITE_PANOSE_ASPECT</a>-typed value that specifies the aspect of the decorative typeface.


### -field decorative.contrast


			
		    A <a href="https://msdn.microsoft.com/EB526A2A-1E85-4A65-B485-4AE87F45C2A0">DWRITE_PANOSE_CONTRAST</a>-typed value that specifies the contrast for the decorative typeface.


### -field decorative.serifVariant


			
		    The serif variant of the decorative typeface.


### -field decorative.fill


			
		    
			
		    A <a href="https://msdn.microsoft.com/787F7193-50E7-46CA-B395-1CFAE2EE3080">DWRITE_PANOSE_FILL</a>-typed value that specifies the fill of the decorative typeface.


### -field decorative.lining

A <a href="https://msdn.microsoft.com/988F14D9-9609-494C-A8DA-CAC75C30C1F5">DWRITE_PANOSE_LINING</a>-typed value that specifies the lining of the decorative typeface.


### -field decorative.decorativeTopology


			
		    A <a href="https://msdn.microsoft.com/EF54C965-D2EF-491F-85BB-0B527ABED8D1">DWRITE_PANOSE_DECORATIVE_TOPOLOGY</a>-typed value that specifies the decorative topology.


### -field decorative.characterRange

A <a href="https://msdn.microsoft.com/A50F0296-D977-47C5-9E41-9567980B16A6">DWRITE_PANOSE_CHARACTER_RANGES</a>-typed value that specifies the character range of the decorative typeface.


### -field symbol


### -field symbol.familyKind


			
		    The <a href="https://msdn.microsoft.com/library/Hh995028(v=VS.85).aspx">DWRITE_PANOSE_FAMILY_SYMBOL</a> value (5) that specifies symbol typeface classification.


### -field symbol.symbolKind


			
		    A <a href="https://msdn.microsoft.com/474F3CF8-2C94-4267-91A1-4BCDC651DC48">DWRITE_PANOSE_SYMBOL_KIND</a>-typed value that specifies the kind of symbol set.


### -field symbol.weight


			
		    A <a href="https://msdn.microsoft.com/9309C68B-1193-47EF-A577-9DC0EEE18F4C">DWRITE_PANOSE_WEIGHT</a>-typed value that specifies the weight of the symbol typeface.


### -field symbol.spacing


			
		    A <a href="https://msdn.microsoft.com/BA841315-2B57-4B35-A6E4-2343EBE67AC8">DWRITE_PANOSE_SPACING</a>-typed value that specifies the spacing of the symbol typeface.


### -field symbol.aspectRatioAndContrast


			
		    A <a href="https://msdn.microsoft.com/C98F339D-0E45-4140-A44E-BFB0FA980251">DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</a>-typed value that specifies the aspect ratio and contrast of the symbol typeface.


### -field symbol.aspectRatio94


			
		    A <a href="https://msdn.microsoft.com/C98F339D-0E45-4140-A44E-BFB0FA980251">DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</a>-typed value that specifies the aspect ratio 94 of the symbol typeface.


### -field symbol.aspectRatio119


			
		    A <a href="https://msdn.microsoft.com/C98F339D-0E45-4140-A44E-BFB0FA980251">DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</a>-typed value that specifies the aspect ratio 119 of the symbol typeface.


### -field symbol.aspectRatio157


			
		    A <a href="https://msdn.microsoft.com/C98F339D-0E45-4140-A44E-BFB0FA980251">DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</a>-typed value that specifies the aspect ratio 157 of the symbol typeface.


### -field symbol.aspectRatio163


			
		    A <a href="https://msdn.microsoft.com/C98F339D-0E45-4140-A44E-BFB0FA980251">DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</a>-typed value that specifies the aspect ratio 163 of the symbol typeface.


### -field symbol.aspectRatio211


			
		    A <a href="https://msdn.microsoft.com/C98F339D-0E45-4140-A44E-BFB0FA980251">DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</a>-typed value that specifies the aspect ratio 211 of the symbol typeface.


#### - values[10]

A 10-byte array of typeface classification values.


## -remarks



<div class="alert"><b>Note</b>  The <b>familyKind</b> member (index 0) is the only stable entry in the 10-byte array because all the entries that follow can change dynamically depending on the context of the first member.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/8CC6E653-FF82-4BBA-9DDE-F3F4960C4BBB">DWRITE_PANOSE_FAMILY</a>



<a href="https://msdn.microsoft.com/DD31C1D6-4CD2-4ED0-BF9F-CAF587C613E6">IDWriteFont1::GetPanose</a>
 

 

