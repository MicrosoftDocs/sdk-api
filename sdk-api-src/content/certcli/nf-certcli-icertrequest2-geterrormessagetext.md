---
UID: NF:certcli.ICertRequest2.GetErrorMessageText
title: ICertRequest2::GetErrorMessageText (certcli.h)
description: Retrieves the error message text for an HRESULT error code.
helpviewer_keywords: ["CCertRequest object [Security]","GetErrorMessageText method","CR_GEMT_HRESULT_STRING","GetErrorMessageText","GetErrorMessageText method [Security]","GetErrorMessageText method [Security]","CCertRequest object","GetErrorMessageText method [Security]","ICertRequest interface","GetErrorMessageText method [Security]","ICertRequest2 interface","GetErrorMessageText method [Security]","ICertRequest3 interface","ICertRequest interface [Security]","GetErrorMessageText method","ICertRequest2 interface [Security]","GetErrorMessageText method","ICertRequest2.GetErrorMessageText","ICertRequest2::GetErrorMessageText","ICertRequest3 interface [Security]","GetErrorMessageText method","ICertRequest3::GetErrorMessageText","ICertRequest::GetErrorMessageText","Zero (0)","_certsrv_icertrequest2_geterrormessagetext","certcli/ICertRequest2::GetErrorMessageText","certcli/ICertRequest3::GetErrorMessageText","certcli/ICertRequest::GetErrorMessageText","security.icertrequest2_geterrormessagetext"]
old-location: security\icertrequest2_geterrormessagetext.htm
tech.root: security
ms.assetid: eeecaeec-2e06-4d4b-9b85-5fb3ef90944a
ms.date: 12/05/2018
ms.keywords: CCertRequest object [Security],GetErrorMessageText method, CR_GEMT_HRESULT_STRING, GetErrorMessageText, GetErrorMessageText method [Security], GetErrorMessageText method [Security],CCertRequest object, GetErrorMessageText method [Security],ICertRequest interface, GetErrorMessageText method [Security],ICertRequest2 interface, GetErrorMessageText method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetErrorMessageText method, ICertRequest2 interface [Security],GetErrorMessageText method, ICertRequest2.GetErrorMessageText, ICertRequest2::GetErrorMessageText, ICertRequest3 interface [Security],GetErrorMessageText method, ICertRequest3::GetErrorMessageText, ICertRequest::GetErrorMessageText, Zero (0), _certsrv_icertrequest2_geterrormessagetext, certcli/ICertRequest2::GetErrorMessageText, certcli/ICertRequest3::GetErrorMessageText, certcli/ICertRequest::GetErrorMessageText, security.icertrequest2_geterrormessagetext
req.header: certcli.h
req.include-header: Certsrv.h
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
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertRequest2::GetErrorMessageText
 - certcli/ICertRequest2::GetErrorMessageText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertRequest3.GetErrorMessageText
 - ICertRequest2.GetErrorMessageText
 - ICertRequest.GetErrorMessageText
 - CCertRequest.GetErrorMessageText
---

# ICertRequest2::GetErrorMessageText


## -description

The <b>GetErrorMessageText</b> method retrieves the error message text for an <b>HRESULT</b> error code.

 If the error message text is localized, it has been localized on the client.

## -parameters

### -param hrMessage [in]

A value that represents an <b>HRESULT</b> error.

### -param Flags [in]

A <b>LONG</b> value that corresponds to one of the values in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Zero__0_"></a><a id="zero__0_"></a><a id="ZERO__0_"></a><dl>
<dt><b>Zero (0)</b></dt>
</dl>
</td>
<td width="60%">
The error message text will not have the <b>HRESULT</b> hexadecimal and decimal values appended.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_GEMT_HRESULT_STRING"></a><a id="cr_gemt_hresult_string"></a><dl>
<dt><b>CR_GEMT_HRESULT_STRING</b></dt>
</dl>
</td>
<td width="60%">
The error message text will have the <b>HRESULT</b> hexadecimal and decimal values appended.

</td>
</tr>
</table>

### -param pstrErrorMessageText [out]

A pointer to the <b>BSTR</b> that represents the error message text for <i>hrMessage</i>. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is a <b>String</b> that contains the error message text for <i>hrMessage</i>.