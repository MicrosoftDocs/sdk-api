---
UID: NN:msctf.ITfDocumentMgr
title: ITfDocumentMgr (msctf.h)
description: The ITfDocumentMgr interface is implemented by the TSF manager and used by an application or text service to create and manage text contexts. To obtain an instance of this interface call ITfThreadMgr::CreateDocumentMgr.
helpviewer_keywords: ["ITfDocumentMgr","ITfDocumentMgr interface [Text Services Framework]","ITfDocumentMgr interface [Text Services Framework]","described","_tsf_itfdocumentmgr_ref","msctf/ITfDocumentMgr","tsf.itfdocumentmgr"]
old-location: tsf\itfdocumentmgr.htm
tech.root: TSF
ms.assetid: e99e9bdb-6a3a-438d-8fac-92ef96c8dfdd
ms.date: 12/05/2018
ms.keywords: ITfDocumentMgr, ITfDocumentMgr interface [Text Services Framework], ITfDocumentMgr interface [Text Services Framework],described, _tsf_itfdocumentmgr_ref, msctf/ITfDocumentMgr, tsf.itfdocumentmgr
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfDocumentMgr
 - msctf/ITfDocumentMgr
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
 - ITfDocumentMgr
---

# ITfDocumentMgr interface


## -description

The <b>ITfDocumentMgr</b> interface is implemented by the TSF manager and used by an application or text service to create and manage text contexts. To obtain an instance of this interface call <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-createdocumentmgr">ITfThreadMgr::CreateDocumentMgr</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfDocumentMgr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfDocumentMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfDocumentMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">CreateContext</a>
</td>
<td align="left" width="63%">
Creates a context object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-enumcontexts">EnumContexts</a>
</td>
<td align="left" width="63%">
Obtains a context enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-getbase">GetBase</a>
</td>
<td align="left" width="63%">
Obtains the context at the base of the context stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-gettop">GetTop</a>
</td>
<td align="left" width="63%">
Obtains the context at the top of the context stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-pop">Pop</a>
</td>
<td align="left" width="63%">
Removes the context from the top of the context stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-push">Push</a>
</td>
<td align="left" width="63%">
Adds a context to the top of the context stack.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-createdocumentmgr">ITfThreadMgr::CreateDocumentMgr
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

