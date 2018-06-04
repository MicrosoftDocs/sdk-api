---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CryptUIDlgViewContext function


## -description


The <b>CryptUIDlgViewContext</b> function displays a certificate, CTL, or CRL context.


## -parameters




### -param dwContextType [in]

<b>DWORD</b> indicating whether <i>pvContext</i> is a pointer to a certificate, a CRL, or a CTL context as indicated in the following table. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CERTIFICATE_CONTEXT"></a><a id="cert_store_certificate_context"></a><dl>
<dt><b>CERT_STORE_CERTIFICATE_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
PCCERT_CONTEXT

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CRL_CONTEXT"></a><a id="cert_store_crl_context"></a><dl>
<dt><b>CERT_STORE_CRL_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
PCCRL_CONTEXT

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CTL_CONTEXT"></a><a id="cert_store_ctl_context"></a><dl>
<dt><b>CERT_STORE_CTL_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
PCCTL_CONTEXT

</td>
</tr>
</table>
 


### -param pvContext [in]

A pointer to a certificate, CRL, or CTL context to be displayed.


### -param hwnd [in]

Handle of the window for the display. If <b>NULL</b>, the display defaults to the desktop window.


### -param pwszTitle [in]

Display title string. If <b>NULL</b>, the default context type is used as the title.


### -param dwFlags [in]

Currently not used and should be set to 0.


### -param pvReserved [in]

Reserved for future use.


## -returns



This function returns <b>TRUE</b> on success and <b>FALSE</b> on failure.




## -see-also




<a href="https://msdn.microsoft.com/5774af1c-f2d4-4b1e-a20b-dfb57bf9aa37">CryptUIDlgSelectCertificateFromStore</a>
 

 

