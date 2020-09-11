---
UID: NN:msctf.ITfThreadMgr
title: ITfThreadMgr (msctf.h)
description: The ITfThreadMgr defines the primary object implemented by the TSF manager. ITfThreadMgr is used by applications and text services to activate and deactivate text services, create document managers, and maintain the document context focus.
helpviewer_keywords: ["ITfThreadMgr","ITfThreadMgr interface [Text Services Framework]","ITfThreadMgr interface [Text Services Framework]","described","_tsf_itfthreadmgr_ref","msctf/ITfThreadMgr","tsf.itfthreadmgr"]
old-location: tsf\itfthreadmgr.htm
tech.root: TSF
ms.assetid: 3a2ba59c-3565-4f54-ac10-923dcb4882cb
ms.date: 12/05/2018
ms.keywords: ITfThreadMgr, ITfThreadMgr interface [Text Services Framework], ITfThreadMgr interface [Text Services Framework],described, _tsf_itfthreadmgr_ref, msctf/ITfThreadMgr, tsf.itfthreadmgr
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
 - ITfThreadMgr
 - msctf/ITfThreadMgr
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
 - ITfThreadMgr
---

# ITfThreadMgr interface


## -description

The <b>ITfThreadMgr</b> defines the primary object implemented by the TSF manager. <b>ITfThreadMgr</b> is used by applications and text services to activate and deactivate text services, create document managers, and maintain the document context focus.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfThreadMgr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfThreadMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfThreadMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-activate">Activate</a>
</td>
<td align="left" width="63%">
Activates TSF for the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-associatefocus">AssociateFocus</a>
</td>
<td align="left" width="63%">
Associates the focus for a window with a document manager object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-createdocumentmgr">CreateDocumentMgr</a>
</td>
<td align="left" width="63%">
Creates a document manager object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-deactivate">Deactivate</a>
</td>
<td align="left" width="63%">
Deactivates TSF for the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-enumdocumentmgrs">EnumDocumentMgrs</a>
</td>
<td align="left" width="63%">
Returns an enumerator for all the document managers within the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-enumfunctionproviders">EnumFunctionProviders</a>
</td>
<td align="left" width="63%">
Obtains an enumerator for all of the function providers registered for the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-getfocus">GetFocus</a>
</td>
<td align="left" width="63%">
Returns the document manager that has the input focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-getfunctionprovider">GetFunctionProvider</a>
</td>
<td align="left" width="63%">
Obtains the specified function provider object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-getglobalcompartment">GetGlobalCompartment</a>
</td>
<td align="left" width="63%">
Obtains the global compartment manager object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-isthreadfocus">IsThreadFocus</a>
</td>
<td align="left" width="63%">
Determines if the calling thread has the TSF input focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-setfocus">SetFocus</a>
</td>
<td align="left" width="63%">
Sets the input focus to the specified document manager.

</td>
</tr>
</table>

## -remarks

An application obtains a pointer to this interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with CLSID_TF_ThreadMgr as demonstrated below.

A text service receives a pointer to this interface in its <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate">ITfTextInputProcessor::Activate</a> method.


#### Examples


```cpp

HRESULT hr;
ITfThreadMgr* pThreadMgr;

hr = CoCreateInstance(  CLSID_TF_ThreadMgr, 
                        NULL, 
                        CLSCTX_INPROC_SERVER, 
                        IID_ITfThreadMgr, 
                        (void**)&pThreadMgr);

```

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate">ITfTextInputProcessor::Activate
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

