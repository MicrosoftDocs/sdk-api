---
UID: NF:ctffunc.ITfFnPropertyUIStatus.SetStatus
title: ITfFnPropertyUIStatus::SetStatus (ctffunc.h)
description: ITfFnPropertyUIStatus::SetStatus method
helpviewer_keywords: ["ITfFnPropertyUIStatus interface [Text Services Framework]","SetStatus method","ITfFnPropertyUIStatus.SetStatus","ITfFnPropertyUIStatus::SetStatus","SetStatus","SetStatus method [Text Services Framework]","SetStatus method [Text Services Framework]","ITfFnPropertyUIStatus interface","_tsf_itffnpropertyuistatus_setstatus_ref","ctffunc/ITfFnPropertyUIStatus::SetStatus","tsf.itffnpropertyuistatus_setstatus"]
old-location: tsf\itffnpropertyuistatus_setstatus.htm
tech.root: TSF
ms.assetid: 817329fb-521a-426a-88d8-b36ee161b6b9
ms.date: 12/05/2018
ms.keywords: ITfFnPropertyUIStatus interface [Text Services Framework],SetStatus method, ITfFnPropertyUIStatus.SetStatus, ITfFnPropertyUIStatus::SetStatus, SetStatus, SetStatus method [Text Services Framework], SetStatus method [Text Services Framework],ITfFnPropertyUIStatus interface, _tsf_itffnpropertyuistatus_setstatus_ref, ctffunc/ITfFnPropertyUIStatus::SetStatus, tsf.itffnpropertyuistatus_setstatus
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
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
 - ITfFnPropertyUIStatus::SetStatus
 - ctffunc/ITfFnPropertyUIStatus::SetStatus
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
 - ITfFnPropertyUIStatus.SetStatus
---

# ITfFnPropertyUIStatus::SetStatus


## -description

Modifies the status of a text service property UI.

## -parameters

### -param refguidProp [in]

Specifies the property identifier. This can be a custom identifier or one of the <a href="/windows/desktop/TSF/predefined-properties">predefined property</a> identifiers.

### -param dw [in]

Contains the new property UI status. See the <i>pdw</i> parameter of <a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus">ITfFnPropertyUIStatus::GetStatus</a> for possible values.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The text service does not support this method.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffnpropertyuistatus">ITfFnPropertyUIStatus</a>



<a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus">ITfFnPropertyUIStatus::GetStatus
      </a>



<a href="/windows/desktop/TSF/predefined-properties">Predefined Properties
      </a>