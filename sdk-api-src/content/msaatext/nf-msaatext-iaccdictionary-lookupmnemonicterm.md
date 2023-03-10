---
UID: NF:msaatext.IAccDictionary.LookupMnemonicTerm
title: IAccDictionary::LookupMnemonicTerm (msaatext.h)
description: Clients call the IAccDictionary::LookupMnemonicTerm method to find the property for a given mnemonic string.
helpviewer_keywords: ["IAccDictionary interface [Windows Accessibility]","LookupMnemonicTerm method","IAccDictionary.LookupMnemonicTerm","IAccDictionary::LookupMnemonicTerm","LookupMnemonicTerm","LookupMnemonicTerm method [Windows Accessibility]","LookupMnemonicTerm method [Windows Accessibility]","IAccDictionary interface","_msaa_IAccDictionary_LookupMnemonicTerm","msaa.iaccdictionary_iaccdictionary__lookupmnemonicterm","msaatext/IAccDictionary::LookupMnemonicTerm","winauto.iaccdictionary_iaccdictionary__lookupmnemonicterm"]
old-location: winauto\iaccdictionary_iaccdictionary__lookupmnemonicterm.htm
tech.root: WinAuto
ms.assetid: a8a4dfde-3721-4bf5-a609-12f06154b5f0
ms.date: 12/05/2018
ms.keywords: IAccDictionary interface [Windows Accessibility],LookupMnemonicTerm method, IAccDictionary.LookupMnemonicTerm, IAccDictionary::LookupMnemonicTerm, LookupMnemonicTerm, LookupMnemonicTerm method [Windows Accessibility], LookupMnemonicTerm method [Windows Accessibility],IAccDictionary interface, _msaa_IAccDictionary_LookupMnemonicTerm, msaa.iaccdictionary_iaccdictionary__lookupmnemonicterm, msaatext/IAccDictionary::LookupMnemonicTerm, winauto.iaccdictionary_iaccdictionary__lookupmnemonicterm
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
 - IAccDictionary::LookupMnemonicTerm
 - msaatext/IAccDictionary::LookupMnemonicTerm
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
 - IAccDictionary.LookupMnemonicTerm
---

# IAccDictionary::LookupMnemonicTerm


## -description

Clients call the <b>IAccDictionary::LookupMnemonicTerm</b> method to find the property for a given mnemonic string.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="/windows/win32/tsf/text-services-framework">Microsoft Windows Text Services Framework</a> for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters

### -param bstrMnemonic [in]

Type: <b>BSTR</b>

A non-localized mnemonic string for a property.

### -param pTerm [out]

Type: <b>GUID*</b>

A GUID representing the property in <i>bstrMnemonic</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

## -remarks

If the <i>bstrMnemonic</i> parameter is not found in the dictionary, then <i>pTerm</i> will be <b>NULL</b>.