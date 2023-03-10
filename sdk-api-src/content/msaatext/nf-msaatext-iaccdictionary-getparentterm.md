---
UID: NF:msaatext.IAccDictionary.GetParentTerm
title: IAccDictionary::GetParentTerm (msaatext.h)
description: Clients call the IAccDictionary::GetParentTerm method to navigate through the object hierarchy tree. This method returns the parent object of a specified property.
helpviewer_keywords: ["GetParentTerm","GetParentTerm method [Windows Accessibility]","GetParentTerm method [Windows Accessibility]","IAccDictionary interface","IAccDictionary interface [Windows Accessibility]","GetParentTerm method","IAccDictionary.GetParentTerm","IAccDictionary::GetParentTerm","_msaa_IAccDictionary_GetParentTerm","msaa.iaccdictionary_iaccdictionary__getparentterm","msaatext/IAccDictionary::GetParentTerm","winauto.iaccdictionary_iaccdictionary__getparentterm"]
old-location: winauto\iaccdictionary_iaccdictionary__getparentterm.htm
tech.root: WinAuto
ms.assetid: 202058e8-50c2-4366-9bb6-bbc46dc5ea3f
ms.date: 12/05/2018
ms.keywords: GetParentTerm, GetParentTerm method [Windows Accessibility], GetParentTerm method [Windows Accessibility],IAccDictionary interface, IAccDictionary interface [Windows Accessibility],GetParentTerm method, IAccDictionary.GetParentTerm, IAccDictionary::GetParentTerm, _msaa_IAccDictionary_GetParentTerm, msaa.iaccdictionary_iaccdictionary__getparentterm, msaatext/IAccDictionary::GetParentTerm, winauto.iaccdictionary_iaccdictionary__getparentterm
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
 - IAccDictionary::GetParentTerm
 - msaatext/IAccDictionary::GetParentTerm
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
 - IAccDictionary.GetParentTerm
---

# IAccDictionary::GetParentTerm


## -description

Clients call the <b>IAccDictionary::GetParentTerm</b> method to navigate through the object hierarchy tree. This method returns the parent object of a specified property.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="/windows/win32/tsf/text-services-framework">Microsoft Windows Text Services Framework</a> for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters

### -param Term [in]

Type: <b>REFGUID</b>

A GUID for a property.

### -param pParentTerm [out]

Type: <b>GUID*</b>

The parent of the property specified in the <i>Term</i> parameter.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

## -remarks

If there is not a parent term for <i>Term</i>, then <i>pParentTerm</i> will point to GUID_NULL.