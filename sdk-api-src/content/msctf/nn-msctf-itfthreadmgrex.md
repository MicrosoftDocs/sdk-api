---
UID: NN:msctf.ITfThreadMgrEx
title: ITfThreadMgrEx (msctf.h)
description: The ITfThreadMgrEx interface is used by the application to activate the textservices with some flags. ITfThreadMgrEx can be obtained by QI from ITfThreadMgr.
helpviewer_keywords: ["ITfThreadMgrEx","ITfThreadMgrEx interface [Text Services Framework]","ITfThreadMgrEx interface [Text Services Framework]","described","_tsf_itfthreadmgrex_ref","msctf/ITfThreadMgrEx","tsf.itfthreadmgrex"]
old-location: tsf\itfthreadmgrex.htm
tech.root: TSF
ms.assetid: c230c363-3c62-459f-9350-d96db916f29c
ms.date: 12/05/2018
ms.keywords: ITfThreadMgrEx, ITfThreadMgrEx interface [Text Services Framework], ITfThreadMgrEx interface [Text Services Framework],described, _tsf_itfthreadmgrex_ref, msctf/ITfThreadMgrEx, tsf.itfthreadmgrex
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfThreadMgrEx
 - msctf/ITfThreadMgrEx
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
 - ITfThreadMgrEx
---

# ITfThreadMgrEx interface


## -description

The <b>ITfThreadMgrEx</b> interface is used by the application to activate the textservices with some flags. ITfThreadMgrEx can be obtained by QI from <a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfThreadMgrEx</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfThreadMgrEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfThreadMgrEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgrex-activateex">ActivateEx</a>
</td>
<td align="left" width="63%">
Activates TSF for the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags">GetActiveFlags</a>
</td>
<td align="left" width="63%">
Gets the active flags of the calling thread.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr
      </a>