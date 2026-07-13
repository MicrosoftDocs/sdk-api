---
UID: NF:msaatext.IAccClientDocMgr.LookupByHWND
title: IAccClientDocMgr::LookupByHWND (msaatext.h)
description: Clients call IAccClientDocMgr::LookupByHWND to get a document by providing the HWND for the document.
helpviewer_keywords: ["IAccClientDocMgr interface [Windows Accessibility]","LookupByHWND method","IAccClientDocMgr.LookupByHWND","IAccClientDocMgr::LookupByHWND","LookupByHWND","LookupByHWND method [Windows Accessibility]","LookupByHWND method [Windows Accessibility]","IAccClientDocMgr interface","_msaa_IAccClientDocMgr_LookupByHWND","msaa.iaccclientdocmgr_iaccclientdocmgr__lookupbyhwnd","msaatext/IAccClientDocMgr::LookupByHWND","winauto.iaccclientdocmgr_iaccclientdocmgr__lookupbyhwnd"]
old-location: winauto\iaccclientdocmgr_iaccclientdocmgr__lookupbyhwnd.htm
tech.root: WinAuto
ms.assetid: fb67c208-b79b-4219-ba5b-2235ae4a1dcf
ms.date: 12/05/2018
ms.keywords: IAccClientDocMgr interface [Windows Accessibility],LookupByHWND method, IAccClientDocMgr.LookupByHWND, IAccClientDocMgr::LookupByHWND, LookupByHWND, LookupByHWND method [Windows Accessibility], LookupByHWND method [Windows Accessibility],IAccClientDocMgr interface, _msaa_IAccClientDocMgr_LookupByHWND, msaa.iaccclientdocmgr_iaccclientdocmgr__lookupbyhwnd, msaatext/IAccClientDocMgr::LookupByHWND, winauto.iaccclientdocmgr_iaccclientdocmgr__lookupbyhwnd
req.header: msaatext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msaatext.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
ms.custom: 19H1
f1_keywords:
 - IAccClientDocMgr::LookupByHWND
 - msaatext/IAccClientDocMgr::LookupByHWND
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msaatext.dll
api_name:
 - IAccClientDocMgr.LookupByHWND
---

# IAccClientDocMgr::LookupByHWND


## -description

Clients call <b>IAccClientDocMgr::LookupByHWND</b> to get a document by providing the <b>HWND</b> for the document.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="/windows/win32/tsf/text-services-framework">Microsoft Windows Text Services Framework</a> for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters

### -param hWnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The <b>HWND</b> of the document to be returned.

### -param riid [in]

Type: <b>REFIID</b>

IID of the document being requested. This is usually IID_ITextStoreAnchor.

### -param ppunk [out]

Type: <b>IUnknown*</b>

Interface pointer to the document being requested.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

If not successful, returns the following value or another standard COM error code.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
If the <b>HWND</b> does not correspond to an active document, then <i>ppunk</i> will be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Servers might need to poll this method more than once before they receive a document. There can be a limited time lapse (approximately second) between when a document appears in the system and when it is registered with document services.