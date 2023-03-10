---
UID: NN:msctf.ITfInputProcessorProfileMgr
title: ITfInputProcessorProfileMgr (msctf.h)
description: The ITfInputProcessorProfileMgr interface is implemented by the TSF manager and used by an application or text service to manipulate the language profile of one or more text services.
helpviewer_keywords: ["ITfInputProcessorProfileMgr","ITfInputProcessorProfileMgr interface [Text Services Framework]","ITfInputProcessorProfileMgr interface [Text Services Framework]","described","_tsf_itfinputprocessorprofilemgr_ref","msctf/ITfInputProcessorProfileMgr","tsf.itfinputprocessorprofilemgr"]
old-location: tsf\itfinputprocessorprofilemgr.htm
tech.root: TSF
ms.assetid: d60bb748-3c61-466d-9c17-df7bc4904994
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfileMgr, ITfInputProcessorProfileMgr interface [Text Services Framework], ITfInputProcessorProfileMgr interface [Text Services Framework],described, _tsf_itfinputprocessorprofilemgr_ref, msctf/ITfInputProcessorProfileMgr, tsf.itfinputprocessorprofilemgr
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfInputProcessorProfileMgr
 - msctf/ITfInputProcessorProfileMgr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.h
api_name:
 - ITfInputProcessorProfileMgr
---

# ITfInputProcessorProfileMgr interface


## -description

The <b>ITfInputProcessorProfileMgr</b> interface is implemented by the TSF manager and used by an application or text service to manipulate the language profile of one or more text services.

## -inheritance

The <b>ITfInputProcessorProfileMgr</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfInputProcessorProfileMgr</b> also has these types of members:

## -remarks

Unlike <a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a>, ITfInputProcessorProfileMgr
 can manage both keyboard layout and text services seamlessly. In Windows Vista, it is recommended to use this interface instead of using the following methods:

<ul>
<li>ITfInputProcessorProfiles::Register</li>
<li>ITfInputProcessorProfiles::Unregister</li>
<li>ITfInputProcessorProfiles::AddLanguageProfile</li>
<li>ITfInputProcessorProfiles::RemoveLanguageProfile</li>
<li>ITfInputProcessorProfiles::EnumInputProcessorInfo</li>
<li>ITfInputProcessorProfiles::ActivateLanguageProfile</li>
<li>ITfInputProcessorProfiles::GetActiveLanguageProfile</li>
<li>ITfInputProcessorProfiles::EnumLanguageProfiles</li>
</ul>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a>
