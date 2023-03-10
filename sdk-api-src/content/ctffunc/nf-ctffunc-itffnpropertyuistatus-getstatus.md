---
UID: NF:ctffunc.ITfFnPropertyUIStatus.GetStatus
title: ITfFnPropertyUIStatus::GetStatus (ctffunc.h)
description: ITfFnPropertyUIStatus::GetStatus method
helpviewer_keywords: ["GetStatus","GetStatus method [Text Services Framework]","GetStatus method [Text Services Framework]","ITfFnPropertyUIStatus interface","ITfFnPropertyUIStatus interface [Text Services Framework]","GetStatus method","ITfFnPropertyUIStatus.GetStatus","ITfFnPropertyUIStatus::GetStatus","TF_PROPUI_STATUS_SAVETOFILE","_tsf_itffnpropertyuistatus_getstatus_ref","ctffunc/ITfFnPropertyUIStatus::GetStatus","tsf.itffnpropertyuistatus_getstatus"]
old-location: tsf\itffnpropertyuistatus_getstatus.htm
tech.root: TSF
ms.assetid: aef8c1b4-3cda-4fa3-ae8c-a8f8da4840b5
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Text Services Framework], GetStatus method [Text Services Framework],ITfFnPropertyUIStatus interface, ITfFnPropertyUIStatus interface [Text Services Framework],GetStatus method, ITfFnPropertyUIStatus.GetStatus, ITfFnPropertyUIStatus::GetStatus, TF_PROPUI_STATUS_SAVETOFILE, _tsf_itffnpropertyuistatus_getstatus_ref, ctffunc/ITfFnPropertyUIStatus::GetStatus, tsf.itffnpropertyuistatus_getstatus
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
 - ITfFnPropertyUIStatus::GetStatus
 - ctffunc/ITfFnPropertyUIStatus::GetStatus
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
 - ITfFnPropertyUIStatus.GetStatus
---

# ITfFnPropertyUIStatus::GetStatus


## -description

Obtains the status of a text service property UI.

## -parameters

### -param refguidProp [in]

Specifies the property identifier. This can be a custom identifier or one of the <a href="/windows/desktop/TSF/predefined-properties">predefined property</a> identifiers.

### -param pdw [out]

Pointer to a <b>DWORD</b> that receives the property UI status. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_PROPUI_STATUS_SAVETOFILE"></a><a id="tf_propui_status_savetofile"></a><dl>
<dt><b>TF_PROPUI_STATUS_SAVETOFILE</b></dt>
</dl>
</td>
<td width="60%">
The property can be serialized. If this value is not present, the property cannot be serialized.

</td>
</tr>
</table>

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
<i>pdw</i> is invalid.

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



<a href="/windows/desktop/TSF/predefined-properties">Predefined Properties
      </a>