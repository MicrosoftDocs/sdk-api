---
UID: NF:msaatext.IAccClientDocMgr.LookupByPoint
title: IAccClientDocMgr::LookupByPoint (msaatext.h)
description: Clients call IAccClientDocMgr::LookupByPoint to get a document object from a point within the document.
helpviewer_keywords: ["IAccClientDocMgr interface [Windows Accessibility]","LookupByPoint method","IAccClientDocMgr.LookupByPoint","IAccClientDocMgr::LookupByPoint","LookupByPoint","LookupByPoint method [Windows Accessibility]","LookupByPoint method [Windows Accessibility]","IAccClientDocMgr interface","_msaa_IAccClientDocMgr_LookupByPoint","msaa.iaccclientdocmgr_iaccclientdocmgr__lookupbypoint","msaatext/IAccClientDocMgr::LookupByPoint","winauto.iaccclientdocmgr_iaccclientdocmgr__lookupbypoint"]
old-location: winauto\iaccclientdocmgr_iaccclientdocmgr__lookupbypoint.htm
tech.root: WinAuto
ms.assetid: 6de40049-3c61-458c-b7e0-c4b416780581
ms.date: 12/05/2018
ms.keywords: IAccClientDocMgr interface [Windows Accessibility],LookupByPoint method, IAccClientDocMgr.LookupByPoint, IAccClientDocMgr::LookupByPoint, LookupByPoint, LookupByPoint method [Windows Accessibility], LookupByPoint method [Windows Accessibility],IAccClientDocMgr interface, _msaa_IAccClientDocMgr_LookupByPoint, msaa.iaccclientdocmgr_iaccclientdocmgr__lookupbypoint, msaatext/IAccClientDocMgr::LookupByPoint, winauto.iaccclientdocmgr_iaccclientdocmgr__lookupbypoint
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
 - IAccClientDocMgr::LookupByPoint
 - msaatext/IAccClientDocMgr::LookupByPoint
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
 - IAccClientDocMgr.LookupByPoint
---

# IAccClientDocMgr::LookupByPoint


## -description

Clients call <b>IAccClientDocMgr::LookupByPoint</b> to get a document object from a point within the document.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="/windows/win32/tsf/text-services-framework">Microsoft Windows Text Services Framework</a> for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters

### -param pt [in]

Type: <b>POINT</b>

A point inside the bounding rectangle of the document to be returned.

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
If the value in <i>pt</i> does not fall within the bounding rectangle of an active document, then <i>ppunk</i> will be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Servers might need to poll this method more than once before they receive a document. There can be a limited time lapse (approximately second) between when a document appears in the system and when it is registered with document services.