---
UID: NF:gdiplusstringformat.StringFormat.GetDigitSubstitutionLanguage
title: StringFormat::GetDigitSubstitutionLanguage
author: windows-sdk-content
description: The StringFormat::GetDigitSubstitutionLanguage method gets the language that corresponds with the digits that are to be substituted for Western European digits.
old-location: gdiplus\_gdiplus_CLASS_StringFormat_GetDigitSubstitutionLanguage_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\getdigitsubstitutionlanguage.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetDigitSubstitutionLanguage, GetDigitSubstitutionLanguage method [GDI+], GetDigitSubstitutionLanguage method [GDI+],StringFormat class, StringFormat class [GDI+],GetDigitSubstitutionLanguage method, StringFormat.GetDigitSubstitutionLanguage, StringFormat::GetDigitSubstitutionLanguage, _gdiplus_CLASS_StringFormat_GetDigitSubstitutionLanguage_, gdiplus._gdiplus_CLASS_StringFormat_GetDigitSubstitutionLanguage_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	StringFormat.GetDigitSubstitutionLanguage
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# StringFormat::GetDigitSubstitutionLanguage


## -description


The <b>StringFormat::GetDigitSubstitutionLanguage</b> method gets the language that corresponds with the digits that are to be substituted for Western European digits.


## -parameters






## -returns



Type: <strong>Type: <b>LANGID</b>
</strong>

This method returns a 16-bit value that forms a National Language Support (NLS) language identifier. This identifier indicates the language that corresponds with the substitution digits. For example, if this 
						<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a> object uses Arabic substitution digits, then this method will return a value that indicates an Arabic language. An NLS language identifier is constructed by the MAKELANGID macro declared in Winnt.h.



