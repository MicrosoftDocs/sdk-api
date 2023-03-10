---
UID: NF:msaatext.IAccDictionary.ConvertValueToString
title: IAccDictionary::ConvertValueToString (msaatext.h)
description: Clients call the IAccDictionary::ConvertValueToString method to convert a value to a localized string.
helpviewer_keywords: ["ConvertValueToString","ConvertValueToString method [Windows Accessibility]","ConvertValueToString method [Windows Accessibility]","IAccDictionary interface","IAccDictionary interface [Windows Accessibility]","ConvertValueToString method","IAccDictionary.ConvertValueToString","IAccDictionary::ConvertValueToString","_msaa_IAccDictionary_ConvertValueToString","msaa.iaccdictionary_iaccdictionary__convertvaluetostring","msaatext/IAccDictionary::ConvertValueToString","winauto.iaccdictionary_iaccdictionary__convertvaluetostring"]
old-location: winauto\iaccdictionary_iaccdictionary__convertvaluetostring.htm
tech.root: WinAuto
ms.assetid: 30ac7ba4-9968-40dd-99d2-8600d25ade20
ms.date: 12/05/2018
ms.keywords: ConvertValueToString, ConvertValueToString method [Windows Accessibility], ConvertValueToString method [Windows Accessibility],IAccDictionary interface, IAccDictionary interface [Windows Accessibility],ConvertValueToString method, IAccDictionary.ConvertValueToString, IAccDictionary::ConvertValueToString, _msaa_IAccDictionary_ConvertValueToString, msaa.iaccdictionary_iaccdictionary__convertvaluetostring, msaatext/IAccDictionary::ConvertValueToString, winauto.iaccdictionary_iaccdictionary__convertvaluetostring
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
 - IAccDictionary::ConvertValueToString
 - msaatext/IAccDictionary::ConvertValueToString
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
 - IAccDictionary.ConvertValueToString
---

# IAccDictionary::ConvertValueToString


## -description

Clients call the <b>IAccDictionary::ConvertValueToString</b> method to convert a value to a localized string.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="/windows/win32/tsf/text-services-framework">Microsoft Windows Text Services Framework</a> for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters

### -param Term [in]

Type: <b>REFGUID</b>

A GUID that represents a property.

### -param lcid [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LCID</a></b>

The locale of the string to be returned.

### -param varValue [in]

Type: <b>VARIANT</b>

The value of the item.

### -param pbstrResult [out]

Type: <b>BSTR*</b>

A pointer to the converted value.

### -param plcid [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LCID</a>*</b>

A pointer to the language of the returned string.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

## -remarks

If the <i>Term</i> parameter can be true or false, <b>ConvertValueToString</b> will return a localized string or <b>TRUE</b> or <b>FALSE</b>. If the <i>Term</i> parameter represents a color, <b>ConvertValueToString</b> will return a string for the closest color name. If the <i>Term</i> parameter is not found in the dictionary, then <i>pbstrResult</i> will be <b>NULL</b>.