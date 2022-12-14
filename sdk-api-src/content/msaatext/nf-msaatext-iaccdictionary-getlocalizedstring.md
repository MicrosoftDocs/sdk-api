---
UID: NF:msaatext.IAccDictionary.GetLocalizedString
title: IAccDictionary::GetLocalizedString (msaatext.h)
description: Clients call the IAccDictionary::GetLocalizedString method to get localized strings for all system properties and their values.
helpviewer_keywords: ["GetLocalizedString","GetLocalizedString method [Windows Accessibility]","GetLocalizedString method [Windows Accessibility]","IAccDictionary interface","IAccDictionary interface [Windows Accessibility]","GetLocalizedString method","IAccDictionary.GetLocalizedString","IAccDictionary::GetLocalizedString","_msaa_IAccDictionary_GetLocalizedString","msaa.iaccdictionary_iaccdictionary__getlocalizedstring","msaatext/IAccDictionary::GetLocalizedString","winauto.iaccdictionary_iaccdictionary__getlocalizedstring"]
old-location: winauto\iaccdictionary_iaccdictionary__getlocalizedstring.htm
tech.root: WinAuto
ms.assetid: 7419395d-d4be-4ee4-bf98-aef7e82cb3d5
ms.date: 12/05/2018
ms.keywords: GetLocalizedString, GetLocalizedString method [Windows Accessibility], GetLocalizedString method [Windows Accessibility],IAccDictionary interface, IAccDictionary interface [Windows Accessibility],GetLocalizedString method, IAccDictionary.GetLocalizedString, IAccDictionary::GetLocalizedString, _msaa_IAccDictionary_GetLocalizedString, msaa.iaccdictionary_iaccdictionary__getlocalizedstring, msaatext/IAccDictionary::GetLocalizedString, winauto.iaccdictionary_iaccdictionary__getlocalizedstring
req.header: msaatext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Msaatext.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
ms.custom: 19H1
f1_keywords:
 - IAccDictionary::GetLocalizedString
 - msaatext/IAccDictionary::GetLocalizedString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msaatext.dll
api_name:
 - IAccDictionary.GetLocalizedString
---

# IAccDictionary::GetLocalizedString


## -description

Clients call the <b>IAccDictionary::GetLocalizedString</b> method to get localized strings for all system properties and their values.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="/windows/win32/tsf/text-services-framework">Microsoft Windows Text Services Framework</a> for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters

### -param Term [in]

Type: <b>REFGUID</b>

A globally unique identifier (GUID) that represents a property.

### -param lcid [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LCID</a></b>

The locale of the string to be returned.

### -param pResult [out]

Type: <b>BSTR*</b>

A localized string that represents the term.

### -param plcid [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LCID</a>*</b>

The language of the returned string.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

## -remarks

This method returns the names of a property in the language specified by <i>lcid</i>. If that language is not on the system, Microsoft Active Accessibility finds the best match and returns the string in that language. If the <i>Term</i> parameter is not found in the dictionary, the <i>pResult</i> will be <b>NULL</b>.