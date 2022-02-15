---
UID: NN:msctf.ITfInputProcessorProfilesEx
title: ITfInputProcessorProfilesEx (msctf.h)
description: This interface is implemented by the TSF manager and used by a text service or application to set the display description of the language profile.
helpviewer_keywords: ["ITfInputProcessorProfilesEx","ITfInputProcessorProfilesEx interface [Text Services Framework]","ITfInputProcessorProfilesEx interface [Text Services Framework]","described","msctf/ITfInputProcessorProfilesEx","tsf.itfinputprocessorprofilesex"]
old-location: tsf\itfinputprocessorprofilesex.htm
tech.root: TSF
ms.assetid: c3d811df-dfa4-4de1-abb9-ff0291258c8c
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfilesEx, ITfInputProcessorProfilesEx interface [Text Services Framework], ITfInputProcessorProfilesEx interface [Text Services Framework],described, msctf/ITfInputProcessorProfilesEx, tsf.itfinputprocessorprofilesex
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
 - ITfInputProcessorProfilesEx
 - msctf/ITfInputProcessorProfilesEx
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
 - ITfInputProcessorProfilesEx
---

# ITfInputProcessorProfilesEx interface


## -description

This  interface is implemented by the TSF manager and used by a text service or application to set the display description of the language profile. To obtain an instance of this interface, call <b>ITfInputProcessorProfiles::QueryInterface</b> with <b>IID_ITfInputProcessorProfilesEx</b>.

## -inheritance

The <b>ITfInputProcessorProfilesEx</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfInputProcessorProfilesEx</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
