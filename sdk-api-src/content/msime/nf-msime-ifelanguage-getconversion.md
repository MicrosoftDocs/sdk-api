---
UID: NF:msime.IFELanguage.GetConversion
title: IFELanguage::GetConversion
author: windows-sdk-content
description: Converts the input string (which usually contains the Hiragana character) to converted strings.
old-location: intl\ifelanguage_getconversion.htm
old-project: Intl
ms.assetid: A1FA36C7-6A1A-4B08-BA29-7F7C8FE8DF16
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: GetConversion, GetConversion method [Internationalization for Windows Applications], GetConversion method [Internationalization for Windows Applications],IFELanguage interface, IFELanguage interface [Internationalization for Windows Applications],GetConversion method, IFELanguage.GetConversion, IFELanguage::GetConversion, intl.ifelanguage_getconversion, msime/IFELanguage::GetConversion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msime.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: IMEUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msime.h
api_name:
 - IFELanguage.GetConversion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IFELanguage::GetConversion


## -description


Converts the input string (which usually contains the Hiragana character) to converted strings.


## -parameters




### -param string [in]

A string of phonetic characters to convert.


### -param start [in]

The starting character from which <a href="https://msdn.microsoft.com/9EE1BD9E-2D58-4720-841C-39865375BFE0">IFELanguage</a> begins conversion. The first character of <i>string</i> is represented by 1 (not 0).


### -param length [in]

The number of characters to convert. If this value is -1, all of the remaining characters from <i>start</i>  are converted.


### -param result [out, retval]

The converted string. This string is allocated by <a href="https://msdn.microsoft.com/f98bff39-bc5f-4a81-85d7-d5228e20fbc8">SysAllocStringLen</a> and must be freed by the client.


## -returns



<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.




## -see-also




<a href="https://msdn.microsoft.com/9EE1BD9E-2D58-4720-841C-39865375BFE0">IFELanguage</a>
 

 

