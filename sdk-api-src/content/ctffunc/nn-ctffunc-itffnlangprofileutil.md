---
UID: NN:ctffunc.ITfFnLangProfileUtil
title: ITfFnLangProfileUtil (ctffunc.h)
description: The ITfFnLangProfileUtil interface is implemented by the speech text service and used to provide utility methods for the speech text service.
helpviewer_keywords: ["ITfFnLangProfileUtil","ITfFnLangProfileUtil interface [Text Services Framework]","ITfFnLangProfileUtil interface [Text Services Framework]","described","_tsf_itffnlangprofileutil_ref","ctffunc/ITfFnLangProfileUtil","tsf.itffnlangprofileutil"]
old-location: tsf\itffnlangprofileutil.htm
tech.root: TSF
ms.assetid: 42dd534d-9786-4276-b227-fee2d58806b7
ms.date: 12/05/2018
ms.keywords: ITfFnLangProfileUtil, ITfFnLangProfileUtil interface [Text Services Framework], ITfFnLangProfileUtil interface [Text Services Framework],described, _tsf_itffnlangprofileutil_ref, ctffunc/ITfFnLangProfileUtil, tsf.itffnlangprofileutil
f1_keywords:
- ctffunc/ITfFnLangProfileUtil
dev_langs:
- c++
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
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
- Msctf.dll
api_name:
- ITfFnLangProfileUtil
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfFnLangProfileUtil interface


## -description


The <b>ITfFnLangProfileUtil</b> interface is implemented by the speech text service and used to provide utility methods for the speech text service. A text service can create an instance of this interface by calling CoCreateInstance with CLSID_SapiLayr and IID_ITfFnLangProfileUtil.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnLangProfileUtil</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFnLangProfileUtil</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFnLangProfileUtil</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnlangprofileutil-isprofileavailableforlang">IsProfileAvailableForLang</a>
</td>
<td align="left" width="63%">
Determines if the speech text service has a profile available for a specific language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnlangprofileutil-registeractiveprofiles">RegisterActiveProfiles</a>
</td>
<td align="left" width="63%">
Causes the speech text service to register its active profiles.

</td>
</tr>
</table> 

