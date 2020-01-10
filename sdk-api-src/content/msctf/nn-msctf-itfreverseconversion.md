---
UID: NN:msctf.ITfReverseConversion
title: ITfReverseConversion (msctf.h)
description: Performs a reverse conversion of a specified string.
old-location: tsf\itfreverseconversion_.htm
tech.root: TSF
ms.assetid: ca2e036a-d0f8-4372-872a-388217050d15
ms.date: 12/05/2018
ms.keywords: ITfReverseConversion, ITfReverseConversion interface [Text Services Framework], ITfReverseConversion interface [Text Services Framework],described, msctf/ITfReverseConversion, tsf.itfreverseconversion_
f1_keywords:
- msctf/ITfReverseConversion
dev_langs:
- c++
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 with SP1 [desktop apps only]
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
- ITfReverseConversion
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITfReverseConversion interface


## -description


<p class="CCE_Message">[<b>ITfReverseConversion</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For internal use only.]

Performs a reverse conversion of a specified string. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfReverseConversion</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfReverseConversion</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfReverseConversion</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreverseconversion-doreverseconversion">DoReverseConversion</a>
</td>
<td align="left" width="63%">
Performs a reverse conversion of the specified string. 

<div class="alert"><b>Note</b>  <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreverseconversion-doreverseconversion">DoReverseConversion</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For internal use only.</div>
<div> </div>
</td>
</tr>
</table> 


## -remarks



A reverse conversion provides the keystroke sequences required to create the specified string.



