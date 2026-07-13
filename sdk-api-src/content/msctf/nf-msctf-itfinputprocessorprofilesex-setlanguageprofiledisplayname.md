---
UID: NF:msctf.ITfInputProcessorProfilesEx.SetLanguageProfileDisplayName
title: ITfInputProcessorProfilesEx::SetLanguageProfileDisplayName (msctf.h)
description: Redistributable:\_Requires TSF 1.0 on Windows 2000.
helpviewer_keywords: ["ITfInputProcessorProfilesEx","ITfInputProcessorProfilesEx interface [Text Services Framework]","SetLanguageProfileDisplayName method","ITfInputProcessorProfilesEx.SetLanguageProfileDisplayName","ITfInputProcessorProfilesEx::SetLanguageProfileDisplayName","SetLanguageProfileDisplayName","SetLanguageProfileDisplayName method [Text Services Framework]","SetLanguageProfileDisplayName method [Text Services Framework]","ITfInputProcessorProfilesEx interface","msctf/ITfInputProcessorProfilesEx::SetLanguageProfileDisplayName","tsf.itfinputprocessorprofilesex_setlanguageprofiledisplayname","tsf.setlanguageprofiledisplayname"]
old-location: tsf\setlanguageprofiledisplayname.htm
tech.root: TSF
ms.assetid: ce762764-dcaf-4419-8ca0-44a8462a848e
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfilesEx, ITfInputProcessorProfilesEx interface [Text Services Framework],SetLanguageProfileDisplayName method, ITfInputProcessorProfilesEx.SetLanguageProfileDisplayName, ITfInputProcessorProfilesEx::SetLanguageProfileDisplayName, SetLanguageProfileDisplayName, SetLanguageProfileDisplayName method [Text Services Framework], SetLanguageProfileDisplayName method [Text Services Framework],ITfInputProcessorProfilesEx interface, msctf/ITfInputProcessorProfilesEx::SetLanguageProfileDisplayName, tsf.itfinputprocessorprofilesex_setlanguageprofiledisplayname, tsf.setlanguageprofiledisplayname
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfInputProcessorProfilesEx::SetLanguageProfileDisplayName
 - msctf/ITfInputProcessorProfilesEx::SetLanguageProfileDisplayName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfInputProcessorProfilesEx.SetLanguageProfileDisplayName
---

# ITfInputProcessorProfilesEx::SetLanguageProfileDisplayName


## -description

Redistributable: Requires TSF 1.0 on Windows 2000.

Header: Declared in Msctf.idl and Msctf.h.

Library: Included as a resource in Msctf.dll.

## -parameters

### -param rclsid

### -param langid

### -param guidProfile

### -param pchFile

### -param cchFile

### -param uResId

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile">ITfInputProcessorProfiles::AddLanguageProfile
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofilesex">ITfInputProcessorProfilesEx</a>