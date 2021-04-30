---
UID: NF:ctffunc.ITfFnSearchCandidateProvider.SetResult
title: ITfFnSearchCandidateProvider::SetResult (ctffunc.h)
description: Provides a text Service or IME with history data when a candidate is chosen by the user.
helpviewer_keywords: ["ITfFnSearchCandidateProvider interface [Text Services Framework]","SetResult method","ITfFnSearchCandidateProvider.SetResult","ITfFnSearchCandidateProvider::SetResult","SetResult","SetResult method [Text Services Framework]","SetResult method [Text Services Framework]","ITfFnSearchCandidateProvider interface","ctffunc/ITfFnSearchCandidateProvider::SetResult","tsf.itffnsearchcandidateprovider_setresult"]
old-location: tsf\itffnsearchcandidateprovider_setresult.htm
tech.root: TSF
ms.assetid: 5C4DA0D3-58FD-4955-9658-29ECD8FECEC1
ms.date: 12/05/2018
ms.keywords: ITfFnSearchCandidateProvider interface [Text Services Framework],SetResult method, ITfFnSearchCandidateProvider.SetResult, ITfFnSearchCandidateProvider::SetResult, SetResult, SetResult method [Text Services Framework], SetResult method [Text Services Framework],ITfFnSearchCandidateProvider interface, ctffunc/ITfFnSearchCandidateProvider::SetResult, tsf.itffnsearchcandidateprovider_setresult
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfFnSearchCandidateProvider::SetResult
 - ctffunc/ITfFnSearchCandidateProvider::SetResult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ctffunc.h
api_name:
 - ITfFnSearchCandidateProvider.SetResult
---

# ITfFnSearchCandidateProvider::SetResult


## -description

Provides a text Service or IME with history data when a candidate is chosen by the user.

## -parameters

### -param bstrQuery [in]

The reading string for the text service or IME to convert.

### -param bstrApplicationID [in]

App-specified string that enables a text service or IME to optionally provide different candidates to different apps or contexts based on input history. You can pass an empty <b>BSTR</b>, L””, for a generic context.

### -param bstrResult [in]

A string that represents the candidate string chosen by the user.  It should be one of the candidate string values returned by the <a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnsearchcandidateprovider-getsearchcandidates">GetSearchCandidates</a> method.

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
</table>

## -remarks

Implementing and calling the <a href="/windows/desktop/api/ctffunc/nf-ctffunc-itfcandidatelist-setresult">SetResult</a> method is optional.

A text service or IME can return <b>E_PENDING</b> if no corresponding call to <a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnsearchcandidateprovider-getsearchcandidates">GetSearchCandidates</a> has been made yet for the value of <i>bstrQuery</i>.

## -see-also

<a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnsearchcandidateprovider-getsearchcandidates">GetSearchCandidates</a>



<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffnsearchcandidateprovider">ITfFnSearchCandidateProvider</a>