---
UID: NF:msaatext.IAccClientDocMgr.GetDocuments
title: IAccClientDocMgr::GetDocuments (msaatext.h)
description: Clients call IAccClientDocMgr::GetDocuments to get a list of all documents that have been registered with the Microsoft Active Accessibility run time.
helpviewer_keywords: ["GetDocuments","GetDocuments method [Windows Accessibility]","GetDocuments method [Windows Accessibility]","IAccClientDocMgr interface","IAccClientDocMgr interface [Windows Accessibility]","GetDocuments method","IAccClientDocMgr.GetDocuments","IAccClientDocMgr::GetDocuments","_msaa_IAccClientDocMgr_GetDocuments","msaa.iaccclientdocmgr_iaccclientdocmgr__getdocuments","msaatext/IAccClientDocMgr::GetDocuments","winauto.iaccclientdocmgr_iaccclientdocmgr__getdocuments"]
old-location: winauto\iaccclientdocmgr_iaccclientdocmgr__getdocuments.htm
tech.root: WinAuto
ms.assetid: 490a202b-1fb4-4f2e-a8f2-f9134a8a9daf
ms.date: 12/05/2018
ms.keywords: GetDocuments, GetDocuments method [Windows Accessibility], GetDocuments method [Windows Accessibility],IAccClientDocMgr interface, IAccClientDocMgr interface [Windows Accessibility],GetDocuments method, IAccClientDocMgr.GetDocuments, IAccClientDocMgr::GetDocuments, _msaa_IAccClientDocMgr_GetDocuments, msaa.iaccclientdocmgr_iaccclientdocmgr__getdocuments, msaatext/IAccClientDocMgr::GetDocuments, winauto.iaccclientdocmgr_iaccclientdocmgr__getdocuments
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
 - IAccClientDocMgr::GetDocuments
 - msaatext/IAccClientDocMgr::GetDocuments
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
 - IAccClientDocMgr.GetDocuments
---

# IAccClientDocMgr::GetDocuments


## -description

Clients call <b>IAccClientDocMgr::GetDocuments</b> to get a list of all documents that have been registered with the Microsoft Active Accessibility run time.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="/windows/win32/tsf/text-services-framework">Microsoft Windows Text Services Framework</a> for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters

### -param enumUnknown [out]

Type: <b>IEnumUnknown*</b>

A list of document interface pointers.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

## -remarks

Servers might need to poll this method more than once before they receive a document. There can be a limited time lapse (approximately second) between when a document appears in the system and when it is registered with document services.