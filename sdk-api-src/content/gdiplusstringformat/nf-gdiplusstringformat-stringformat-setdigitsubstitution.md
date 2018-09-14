---
UID: NF:gdiplusstringformat.StringFormat.SetDigitSubstitution
title: StringFormat::SetDigitSubstitution
author: windows-sdk-content
description: The StringFormat::SetDigitSubstitution method sets the digit substitution method and the language that corresponds to the digit substitutes.
old-location: gdiplus\_gdiplus_CLASS_StringFormat_SetDigitSubstitution_language_substitute_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\setdigitsubstitution.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: SetDigitSubstitution, SetDigitSubstitution method [GDI+], SetDigitSubstitution method [GDI+],StringFormat class, StringFormat class [GDI+],SetDigitSubstitution method, StringFormat.SetDigitSubstitution, StringFormat::SetDigitSubstitution, _gdiplus_CLASS_StringFormat_SetDigitSubstitution_language_substitute_, gdiplus._gdiplus_CLASS_StringFormat_SetDigitSubstitution_language_substitute_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusstringformat.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - StringFormat.SetDigitSubstitution
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# StringFormat::SetDigitSubstitution


## -description


The <b>StringFormat::SetDigitSubstitution</b> method sets the digit substitution method and the language that corresponds to the digit substitutes. 


## -parameters




### -param language [in]

Type: <b>LANGID</b>

Sixteen-bit value that forms a NLS language identifier. The identifier specifies the language associated with the substitute digits. For example, if this 
					<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a> object uses Arabic substitution digits, then this method will return a value that indicates an Arabic language. An NLS language identifier is constructed by the MAKELANGID macro, declared in Winnt.h. 


### -param substitute [in]

Type: <b><a href="https://msdn.microsoft.com/b61e9a88-2b00-43f5-bc8d-1d6b4d6ecb19">StringDigitSubstitute</a></b>

Element of the 
					<a href="https://msdn.microsoft.com/b61e9a88-2b00-43f5-bc8d-1d6b4d6ecb19">StringDigitSubstitute</a> enumeration that specifies the digit substitution method to be used. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The digit substitution method, specified by an element of the 
				<a href="https://msdn.microsoft.com/b61e9a88-2b00-43f5-bc8d-1d6b4d6ecb19">StringDigitSubstitute</a> enumeration, replaces, in a string, Western European digits with digits that correspond to a user's locale or language.

When specifying LANG_NEUTRAL as the language ID, it is common practice to pass just LANG_NEUTRAL as in the following example:

<code>stat = FontFamily.GetFamilyName(name, LANG_NEUTRAL);</code>

If you are specifying a language other than LANG_NEUTRAL, use MAKELANGID to create the language and sublanguage combination as in the following example: 

<code>LANGID language = MAKELANGID(LANG_CHINESE, SUBLANG_CHINESE_TRADITIONAL);</code>

For a list of the available languages and sublanguages, see Winnt.h.



