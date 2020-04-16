---
UID: NN:msctf.ITfReverseConversionMgr
title: ITfReverseConversionMgr (msctf.h)
description: Provides access to ITfReverseConversion objects, which are used to perform reverse conversions.helpviewer_keywords: ["ITfReverseConversionMgr","ITfReverseConversionMgr interface [Text Services Framework]","ITfReverseConversionMgr interface [Text Services Framework]","described","msctf/ITfReverseConversionMgr","tsf.itfreverseconversionmgr"]
old-location: tsf\itfreverseconversionmgr.htm
tech.root: TSF
ms.assetid: b02f3966-4bbf-4266-b5a5-237d975f69c9
ms.date: 12/05/2018
ms.keywords: ITfReverseConversionMgr, ITfReverseConversionMgr interface [Text Services Framework], ITfReverseConversionMgr interface [Text Services Framework],described, msctf/ITfReverseConversionMgr, tsf.itfreverseconversionmgr
f1_keywords:
- msctf/ITfReverseConversionMgr
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
- ITfReverseConversionMgr
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITfReverseConversionMgr interface


## -description


<p class="CCE_Message">[<b>ITfReverseConversionMgr</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For internal use only.]

Provides access to <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfreverseconversion">ITfReverseConversion</a> objects, which are used to perform reverse conversions. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfReverseConversionMgr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfReverseConversionMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfReverseConversionMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreverseconversionmgr-getreverseconversion">GetReverseConversion</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfreverseconversion">ITfReverseConversion</a> object that can perform reverse conversions. 

<div class="alert"><b>Note</b>  <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreverseconversionmgr-getreverseconversion">GetReverseConversion</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For internal use only.</div>
<div> </div>
</td>
</tr>
</table> 


## -remarks



A reverse conversion provides the keystroke sequences required to create the specified string.



