---
UID: NF:msaatext.IAccClientDocMgr.GetFocused
title: IAccClientDocMgr::GetFocused (msaatext.h)
description: Clients call the IAccClientDocMgr::GetFocused method to access a pointer for the document that has focus.
helpviewer_keywords: ["GetFocused","GetFocused method [Windows Accessibility]","GetFocused method [Windows Accessibility]","IAccClientDocMgr interface","IAccClientDocMgr interface [Windows Accessibility]","GetFocused method","IAccClientDocMgr.GetFocused","IAccClientDocMgr::GetFocused","_msaa_IAccClientDocMgr_GetFocused","msaa.iaccclientdocmgr_iaccclientdocmgr__getfocused","msaatext/IAccClientDocMgr::GetFocused","winauto.iaccclientdocmgr_iaccclientdocmgr__getfocused"]
old-location: winauto\iaccclientdocmgr_iaccclientdocmgr__getfocused.htm
tech.root: WinAuto
ms.assetid: 102a511b-43ad-48c1-8953-647482fa452b
ms.date: 12/05/2018
ms.keywords: GetFocused, GetFocused method [Windows Accessibility], GetFocused method [Windows Accessibility],IAccClientDocMgr interface, IAccClientDocMgr interface [Windows Accessibility],GetFocused method, IAccClientDocMgr.GetFocused, IAccClientDocMgr::GetFocused, _msaa_IAccClientDocMgr_GetFocused, msaa.iaccclientdocmgr_iaccclientdocmgr__getfocused, msaatext/IAccClientDocMgr::GetFocused, winauto.iaccclientdocmgr_iaccclientdocmgr__getfocused
req.header: msaatext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0Windows 98
ms.custom: 19H1
f1_keywords:
 - IAccClientDocMgr::GetFocused
 - msaatext/IAccClientDocMgr::GetFocused
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
 - IAccClientDocMgr.GetFocused
---

# IAccClientDocMgr::GetFocused


## -description

Clients call the <b>IAccClientDocMgr::GetFocused</b> method to access a pointer for the document that has focus.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="/windows/win32/tsf/text-services-framework">Microsoft Windows Text Services Framework</a> for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

IID of the document being requested. This is usually IID_ITextStoreAnchor.

### -param ppunk [out]

Type: <b>IUnknown*</b>

Interface pointer to the document being requested.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

## -remarks

If the window that has focus is not a document that implements the <a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a> interface, <i>ppunk</i> will be <b>NULL</b>.

Servers might need to poll this method more than once before they receive a document. There can be a limited time lapse (approximately second) between when a document appears in the system and when it is registered with document services.