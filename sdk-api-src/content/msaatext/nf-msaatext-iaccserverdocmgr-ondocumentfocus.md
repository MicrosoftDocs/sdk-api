---
UID: NF:msaatext.IAccServerDocMgr.OnDocumentFocus
title: IAccServerDocMgr::OnDocumentFocus (msaatext.h)
description: Applications that use Text Services Framework call IAccServerDocMgr::OnDocumentFocus to notify the Microsoft Active Accessibility run time when a document gets or loses focus.
helpviewer_keywords: ["IAccServerDocMgr interface [Windows Accessibility]","OnDocumentFocus method","IAccServerDocMgr.OnDocumentFocus","IAccServerDocMgr::OnDocumentFocus","OnDocumentFocus","OnDocumentFocus method [Windows Accessibility]","OnDocumentFocus method [Windows Accessibility]","IAccServerDocMgr interface","_msaa_IAccServerDocMgr_OnDocumentFocus","msaa.iaccserverdocmgr_iaccserverdocmgr__ondocumentfocus","msaatext/IAccServerDocMgr::OnDocumentFocus","winauto.iaccserverdocmgr_iaccserverdocmgr__ondocumentfocus"]
old-location: winauto\iaccserverdocmgr_iaccserverdocmgr__ondocumentfocus.htm
tech.root: WinAuto
ms.assetid: 305566ed-20c2-42b6-99c8-108e99f9daeb
ms.date: 12/05/2018
ms.keywords: IAccServerDocMgr interface [Windows Accessibility],OnDocumentFocus method, IAccServerDocMgr.OnDocumentFocus, IAccServerDocMgr::OnDocumentFocus, OnDocumentFocus, OnDocumentFocus method [Windows Accessibility], OnDocumentFocus method [Windows Accessibility],IAccServerDocMgr interface, _msaa_IAccServerDocMgr_OnDocumentFocus, msaa.iaccserverdocmgr_iaccserverdocmgr__ondocumentfocus, msaatext/IAccServerDocMgr::OnDocumentFocus, winauto.iaccserverdocmgr_iaccserverdocmgr__ondocumentfocus
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
 - IAccServerDocMgr::OnDocumentFocus
 - msaatext/IAccServerDocMgr::OnDocumentFocus
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
 - IAccServerDocMgr.OnDocumentFocus
---

# IAccServerDocMgr::OnDocumentFocus


## -description

Applications that use Text Services Framework call <b>IAccServerDocMgr::OnDocumentFocus</b> to notify the Microsoft Active Accessibility run time when a document gets or loses focus. The store keeps this information so that clients can access the document that has focus.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="/windows/win32/tsf/text-services-framework">Microsoft Windows Text Services Framework</a> for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters

### -param punk [in]

Type: <b>IUnknown*</b>

An interface pointer to the document getting focus.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

## -remarks

This can be null indicating that no document has focus.