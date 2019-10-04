---
UID: NF:msime.IFELanguage.GetConversion
title: IFELanguage::GetConversion (msime.h)
author: windows-sdk-content
description: Converts the input string (which usually contains the Hiragana character) to converted strings.
old-location: intl\ifelanguage_getconversion.htm
tech.root: Intl
ms.assetid: A1FA36C7-6A1A-4B08-BA29-7F7C8FE8DF16
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetConversion, GetConversion method [Internationalization for Windows Applications], GetConversion method [Internationalization for Windows Applications],IFELanguage interface, IFELanguage interface [Internationalization for Windows Applications],GetConversion method, IFELanguage.GetConversion, IFELanguage::GetConversion, intl.ifelanguage_getconversion, msime/IFELanguage::GetConversion
ms.topic: method
f1_keywords: 
 - "msime/IFELanguage.GetConversion"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msime.h
api_name:
 - IFELanguage.GetConversion
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFELanguage::GetConversion


## -description


Converts the input string (which usually contains the Hiragana character) to converted strings.


## -parameters




### -param string [in]

A string of phonetic characters to convert.


### -param start [in]

The starting character from which <a href="https://docs.microsoft.com/windows/desktop/api/msime/nn-msime-ifelanguage">IFELanguage</a> begins conversion. The first character of <i>string</i> is represented by 1 (not 0).


### -param length [in]

The number of characters to convert. If this value is -1, all of the remaining characters from <i>start</i>  are converted.


### -param result [out, retval]

The converted string. This string is allocated by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstringlen">SysAllocStringLen</a> and must be freed by the client.


## -returns



<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msime/nn-msime-ifelanguage">IFELanguage</a>
 

 

