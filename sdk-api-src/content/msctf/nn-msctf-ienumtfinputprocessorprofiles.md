---
UID: NN:msctf.IEnumTfInputProcessorProfiles
title: IEnumTfInputProcessorProfiles (msctf.h)
description: The IEnumTfInputProcessorProfiles interface is implemented by TSF manager and used by applications or textservices. This interface can be retrieved by ITfInputProcessorProfileMgr::EnumProfiles and enumerates the registered profiles.helpviewer_keywords: ["IEnumTfInputProcessorProfiles","IEnumTfInputProcessorProfiles interface [Text Services Framework]","IEnumTfInputProcessorProfiles interface [Text Services Framework]","described","_tsf_ienumtfinputprocessorprofiles_ref","msctf/IEnumTfInputProcessorProfiles","tsf.ienumtfinputprocessorprofiles"]
old-location: tsf\ienumtfinputprocessorprofiles.htm
tech.root: TSF
ms.assetid: 1a6dd7f9-d348-4c86-8d74-544aaa45581d
ms.date: 12/05/2018
ms.keywords: IEnumTfInputProcessorProfiles, IEnumTfInputProcessorProfiles interface [Text Services Framework], IEnumTfInputProcessorProfiles interface [Text Services Framework],described, _tsf_ienumtfinputprocessorprofiles_ref, msctf/IEnumTfInputProcessorProfiles, tsf.ienumtfinputprocessorprofiles
f1_keywords:
- msctf/IEnumTfInputProcessorProfiles
dev_langs:
- c++
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Msctf.h
api_name:
- IEnumTfInputProcessorProfiles
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# IEnumTfInputProcessorProfiles interface


## -description


The <b>IEnumTfInputProcessorProfiles</b> interface is implemented by TSF manager and used by applications or textservices. This interface can be retrieved by <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofilemgr-enumprofiles">ITfInputProcessorProfileMgr::EnumProfiles</a> and enumerates the registered profiles.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfInputProcessorProfiles</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTfInputProcessorProfiles</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfInputProcessorProfiles</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfinputprocessorprofiles-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfinputprocessorprofiles-next">Next</a>
</td>
<td align="left" width="63%">
Obtains, from the current position, the specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfinputprocessorprofiles-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfinputprocessorprofiles-skip">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles
      </a>
 

 

