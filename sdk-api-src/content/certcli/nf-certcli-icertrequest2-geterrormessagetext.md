---
UID: NF:certcli.ICertRequest2.GetErrorMessageText
title: ICertRequest2::GetErrorMessageText
author: windows-sdk-content
description: Retrieves the error message text for an HRESULT error code.
old-location: security\icertrequest2_geterrormessagetext.htm
tech.root: seccrypto
ms.assetid: eeecaeec-2e06-4d4b-9b85-5fb3ef90944a
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: CCertRequest object [Security],GetErrorMessageText method, CR_GEMT_HRESULT_STRING, GetErrorMessageText, GetErrorMessageText method [Security], GetErrorMessageText method [Security],CCertRequest object, GetErrorMessageText method [Security],ICertRequest interface, GetErrorMessageText method [Security],ICertRequest2 interface, GetErrorMessageText method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetErrorMessageText method, ICertRequest2 interface [Security],GetErrorMessageText method, ICertRequest2.GetErrorMessageText, ICertRequest2::GetErrorMessageText, ICertRequest3 interface [Security],GetErrorMessageText method, ICertRequest3::GetErrorMessageText, ICertRequest::GetErrorMessageText, Zero (0), _certsrv_icertrequest2_geterrormessagetext, certcli/ICertRequest2::GetErrorMessageText, certcli/ICertRequest3::GetErrorMessageText, certcli/ICertRequest::GetErrorMessageText, security.icertrequest2_geterrormessagetext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

A pointer to the <b>BSTR</b> that represents the error message text for <i>hrMessage</i>. When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is a <b>String</b> that contains the error message text for <i>hrMessage</i>.



