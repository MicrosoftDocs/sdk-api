---
UID: NF:msaatext.IAccDictionary.GetMnemonicString
title: IAccDictionary::GetMnemonicString (msaatext.h)
description: Retrieves a mnemonic string.Note  Active Accessibility Text Services is deprecated.
helpviewer_keywords: ["GetMnemonicString","GetMnemonicString method [Windows Accessibility]","GetMnemonicString method [Windows Accessibility]","IAccDictionary interface","IAccDictionary interface [Windows Accessibility]","GetMnemonicString method","IAccDictionary.GetMnemonicString","IAccDictionary::GetMnemonicString","_msaa_IAccDictionary_GetMnemonicString","msaa.iaccdictionary_iaccdictionary__getmnemonicstring","msaatext/IAccDictionary::GetMnemonicString","winauto.iaccdictionary_iaccdictionary__getmnemonicstring"]
old-location: winauto\iaccdictionary_iaccdictionary__getmnemonicstring.htm
tech.root: WinAuto
ms.assetid: 4855acea-83a9-4752-a780-7f0350a7b137
ms.date: 12/05/2018
ms.keywords: GetMnemonicString, GetMnemonicString method [Windows Accessibility], GetMnemonicString method [Windows Accessibility],IAccDictionary interface, IAccDictionary interface [Windows Accessibility],GetMnemonicString method, IAccDictionary.GetMnemonicString, IAccDictionary::GetMnemonicString, _msaa_IAccDictionary_GetMnemonicString, msaa.iaccdictionary_iaccdictionary__getmnemonicstring, msaatext/IAccDictionary::GetMnemonicString, winauto.iaccdictionary_iaccdictionary__getmnemonicstring
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
 - IAccDictionary::GetMnemonicString
 - msaatext/IAccDictionary::GetMnemonicString
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
 - IAccDictionary.GetMnemonicString
---

# IAccDictionary::GetMnemonicString


## -description

Retrieves a mnemonic string.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="/windows/win32/tsf/text-services-framework">Microsoft Windows Text Services Framework</a> for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters

### -param Term [in]

Type: <b>REFGUID</b>

A GUID representing a property.

### -param pResult [out]

Type: <b>BSTR*</b>

A mnemonic string for the property. This string is not localized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

## -remarks

If the <i>Term</i> parameter is not found in the dictionary, then <i>pResult</i> will be <b>NULL</b>.