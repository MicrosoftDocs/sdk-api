---
UID: NF:msctf.ITfKeystrokeMgr.PreserveKey
title: ITfKeystrokeMgr::PreserveKey (msctf.h)
description: ITfKeystrokeMgr::PreserveKey methodhelpviewer_keywords: ["ITfKeystrokeMgr interface [Text Services Framework]","PreserveKey method","ITfKeystrokeMgr.PreserveKey","ITfKeystrokeMgr::PreserveKey","PreserveKey","PreserveKey method [Text Services Framework]","PreserveKey method [Text Services Framework]","ITfKeystrokeMgr interface","_tsf_itfkeystrokemgr_preservekey_ref","msctf/ITfKeystrokeMgr::PreserveKey","tsf.itfkeystrokemgr_preservekey"]
old-location: tsf\itfkeystrokemgr_preservekey.htm
tech.root: TSF
ms.assetid: ad5cd485-9231-4c29-8977-754dbf25c979
ms.date: 12/05/2018
ms.keywords: ITfKeystrokeMgr interface [Text Services Framework],PreserveKey method, ITfKeystrokeMgr.PreserveKey, ITfKeystrokeMgr::PreserveKey, PreserveKey, PreserveKey method [Text Services Framework], PreserveKey method [Text Services Framework],ITfKeystrokeMgr interface, _tsf_itfkeystrokemgr_preservekey_ref, msctf/ITfKeystrokeMgr::PreserveKey, tsf.itfkeystrokemgr_preservekey
f1_keywords:
- msctf/ITfKeystrokeMgr.PreserveKey
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Msctf.dll
api_name:
- ITfKeystrokeMgr.PreserveKey
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfKeystrokeMgr::PreserveKey


## -description

Registers a preserved key.

## -parameters




### -param tid [in]

Contains the client identifier of the TSF text service. This value is passed to the TSF text service in its <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate">ITfTextInputProcessor::Activate</a> method.


### -param rguid [in]

Contains the command GUID of the preserved key. This value is passed to the TSF text service <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeyeventsink-onpreservedkey">ITfKeyEventSink::OnPreservedKey</a> method to identify the preserved key when the preserved key is activated.


### -param prekey [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/msctf/ns-msctf-tf_preservedkey">TF_PRESERVEDKEY</a> structure that specifies the preserved key. The <b>uVKey</b> member contains the virtual key code and the <b>uModifiers</b> member identifies the modifiers of the preserved key.


### -param pchDesc [in]

Pointer to a Unicode string that contains the description of the preserved key. This cannot be <b>NULL</b> unless <i>cchDesc</i> is zero.


### -param cchDesc [in]

Specifies the number of characters in <i>pchDesc</i>. Pass zero for this parameter if no description is required.


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
<dt><b>TF_E_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The preserved key is registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation error occurred.

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
 




## -remarks



Preserved keys are registered by TSF text services and provide keyboard shortcuts to common commands implemented by the TSF text service.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeyeventsink-onpreservedkey">ITfKeyEventSink::OnPreservedKey
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfkeystrokemgr">ITfKeystrokeMgr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-unpreservekey">ITfKeystrokeMgr::UnpreserveKey
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate">ITfTextInputProcessor::Activate
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/ns-msctf-tf_preservedkey">TF_PRESERVEDKEY
      </a>
 

 

