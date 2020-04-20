---
UID: NN:msctf.ITfInputProcessorProfilesEx
title: ITfInputProcessorProfilesEx (msctf.h)
description: This interface is implemented by the TSF manager and used by a text service or application to set the display description of the language profile.helpviewer_keywords: ["ITfInputProcessorProfilesEx","ITfInputProcessorProfilesEx interface [Text Services Framework]","ITfInputProcessorProfilesEx interface [Text Services Framework]","described","msctf/ITfInputProcessorProfilesEx","tsf.itfinputprocessorprofilesex"]
old-location: tsf\itfinputprocessorprofilesex.htm
tech.root: TSF
ms.assetid: c3d811df-dfa4-4de1-abb9-ff0291258c8c
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfilesEx, ITfInputProcessorProfilesEx interface [Text Services Framework], ITfInputProcessorProfilesEx interface [Text Services Framework],described, msctf/ITfInputProcessorProfilesEx, tsf.itfinputprocessorprofilesex
f1_keywords:
- msctf/ITfInputProcessorProfilesEx
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msctf.dll
api_name:
- ITfInputProcessorProfilesEx
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfInputProcessorProfilesEx interface


## -description


This  interface is implemented by the TSF manager and used by a text service or application to set the display description of the language profile. To obtain an instance of this interface, call <b>ITfInputProcessorProfiles::QueryInterface</b> with <b>IID_ITfInputProcessorProfilesEx</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfInputProcessorProfilesEx</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfInputProcessorProfilesEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfInputProcessorProfilesEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofilesex-setlanguageprofiledisplayname">SetLanguageProfileDisplayName</a>
</td>
<td align="left" width="63%">
Sets the display text  for  an existing language profile from a string resource.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

