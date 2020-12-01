---
UID: NN:msctf.ITfContext
title: ITfContext (msctf.h)
description: The ITfContext interface is implemented by the TSF manager and used by applications and text services to access an edit context.
helpviewer_keywords: ["ITfContext","ITfContext interface [Text Services Framework]","ITfContext interface [Text Services Framework]","described","_tsf_itfcontext_ref","msctf/ITfContext","tsf.itfcontext"]
old-location: tsf\itfcontext.htm
tech.root: TSF
ms.assetid: ca98c7bb-7348-405d-976a-18012b0886c6
ms.date: 12/05/2018
ms.keywords: ITfContext, ITfContext interface [Text Services Framework], ITfContext interface [Text Services Framework],described, _tsf_itfcontext_ref, msctf/ITfContext, tsf.itfcontext
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
 - ITfContext
 - msctf/ITfContext
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
 - ITfContext
---

# ITfContext interface


## -description

The <b>ITfContext</b> interface is implemented by the TSF manager and used by applications and text services to access an edit context.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfContext</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-createrangebackup">CreateRangeBackup</a>
</td>
<td align="left" width="63%">
Creates a backup of a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties">EnumProperties</a>
</td>
<td align="left" width="63%">
Obtains a document property enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/TSF/itfcontext-enumviews">EnumViews</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getactiveview">GetActiveView</a>
</td>
<td align="left" width="63%">
Obtains the active view for the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty">GetAppProperty</a>
</td>
<td align="left" width="63%">
Obtains an application property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getdocumentmgr">GetDocumentMgr</a>
</td>
<td align="left" width="63%">
Obtains the document manager that contains the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getend">GetEnd</a>
</td>
<td align="left" width="63%">
Obtains a range of text positioned at the end of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Obtains a text property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getselection">GetSelection</a>
</td>
<td align="left" width="63%">
Obtains the selection within the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getstart">GetStart</a>
</td>
<td align="left" width="63%">
Obtains a range of text positioned at the beginning of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Obtains the document status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-inwritesession">InWriteSession</a>
</td>
<td align="left" width="63%">
Determines if a client has a read/write lock on the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-requesteditsession">RequestEditSession</a>
</td>
<td align="left" width="63%">
Obtains access to the document text and properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-setselection">SetSelection</a>
</td>
<td align="left" width="63%">
Sets the selection within the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-trackproperties">TrackProperties</a>
</td>
<td align="left" width="63%">
Obtains a special property that can enumerate multiple properties over multiple ranges.

</td>
</tr>
</table>

## -remarks

An edit context object is created by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a>. Often, a text service uses the currently active edit context. The currently active edit context is the edit context at the top of the stack of the active document manager.


#### Examples


```cpp

HRESULT         hr;
ITfDocumentMgr  *pFocusDoc;

hr = pThreadMgr->GetFocus(&pFocusDoc);
if(SUCCEEDED(hr))
{
    ITfContext *pContext;

    hr = pFocusDoc->GetTop(&pContext);
    if(SUCCEEDED(hr))
    {
        //Use the context. 
        
        pContext->Release();
    }

    pFocusDoc->Release();
}

```

## -see-also

<a href="/windows/desktop/TSF/edit-contexts">Edit Contexts</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>