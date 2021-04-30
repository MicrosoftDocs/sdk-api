---
UID: NF:ctfutb.ITfLangBarMgr.GetShowFloatingStatus
title: ITfLangBarMgr::GetShowFloatingStatus (ctfutb.h)
description: ITfLangBarMgr::GetShowFloatingStatus method
helpviewer_keywords: ["GetShowFloatingStatus","GetShowFloatingStatus method [Text Services Framework]","GetShowFloatingStatus method [Text Services Framework]","ITfLangBarMgr interface","ITfLangBarMgr interface [Text Services Framework]","GetShowFloatingStatus method","ITfLangBarMgr.GetShowFloatingStatus","ITfLangBarMgr::GetShowFloatingStatus","_tsf_itflangbarmgr_getshowfloatingstatus_ref","ctfutb/ITfLangBarMgr::GetShowFloatingStatus","tsf.itflangbarmgr_getshowfloatingstatus"]
old-location: tsf\itflangbarmgr_getshowfloatingstatus.htm
tech.root: TSF
ms.assetid: ec187bf0-edf7-4d90-a102-92bb5b58ebdc
ms.date: 12/05/2018
ms.keywords: GetShowFloatingStatus, GetShowFloatingStatus method [Text Services Framework], GetShowFloatingStatus method [Text Services Framework],ITfLangBarMgr interface, ITfLangBarMgr interface [Text Services Framework],GetShowFloatingStatus method, ITfLangBarMgr.GetShowFloatingStatus, ITfLangBarMgr::GetShowFloatingStatus, _tsf_itflangbarmgr_getshowfloatingstatus_ref, ctfutb/ITfLangBarMgr::GetShowFloatingStatus, tsf.itflangbarmgr_getshowfloatingstatus
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
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
 - ITfLangBarMgr::GetShowFloatingStatus
 - ctfutb/ITfLangBarMgr::GetShowFloatingStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfLangBarMgr.GetShowFloatingStatus
---

# ITfLangBarMgr::GetShowFloatingStatus


## -description

Obtains current language bar display settings.

## -parameters

### -param pdwFlags [out]

Indicates current language bar display settings. For a list of bitfield values, see <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-showfloating">ITfLangBarMgr::ShowFloating</a>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwFlags</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbarmgr">ITfLangBarMgr</a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-showfloating">ITfLangBarMgr::ShowFloating
      </a>