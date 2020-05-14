---
UID: NN:msaatext.ITfMSAAControl
title: ITfMSAAControl (msaatext.h)
description: The ITfMSAAControl interface is used by Microsoft Active Accessibility to add or remove a document from TSF control, to avoid unnecessary overhead in TSF. This interface is not recommended for use by other applications.helpviewer_keywords: ["ITfMSAAControl","ITfMSAAControl interface [Text Services Framework]","ITfMSAAControl interface [Text Services Framework]","described","msaatext/ITfMSAAControl","tsf.itfmsaacontrol"]
old-location: tsf\itfmsaacontrol.htm
tech.root: TSF
ms.assetid: e01a0177-7e3a-4087-84b8-151da2145be8
ms.date: 12/05/2018
ms.keywords: ITfMSAAControl, ITfMSAAControl interface [Text Services Framework], ITfMSAAControl interface [Text Services Framework],described, msaatext/ITfMSAAControl, tsf.itfmsaacontrol
f1_keywords:
- msaatext/ITfMSAAControl
dev_langs:
- c++
req.header: msaatext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MSAAText.idl
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
- ITfMSAAControl
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfMSAAControl interface


## -description


The <b>ITfMSAAControl</b> interface is used by <a href="/previous-versions/ms971350(v=msdn.10)">Microsoft Active Accessibility</a> to add or remove a document from TSF control, to avoid unnecessary overhead in TSF. This interface is not recommended for use by other applications.

The interface ID is IID_ITfMSAAControl.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfMSAAControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfMSAAControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfMSAAControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msaatext/nf-msaatext-itfmsaacontrol-systemdisablemsaa">SystemDisableMSAA</a>
</td>
<td align="left" width="63%">
Used by MSAA to halt TSF support of an MSAA client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msaatext/nf-msaatext-itfmsaacontrol-systemenablemsaa">SystemEnableMSAA</a>
</td>
<td align="left" width="63%">
Used by MSAA to request TSF support of an MSAA client.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/previous-versions/ms971350(v=msdn.10)">Microsoft Active Accessibility</a>
 

 

