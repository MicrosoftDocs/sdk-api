---
UID: NF:certcli.ICertRequest3.GetRequestIdString
title: ICertRequest3::GetRequestIdString
author: windows-sdk-content
description: Gets the current internal request number, formatted as a string, for the request and subsequent certificate.
old-location: security\icertrequest3_getrequestidstring.htm
tech.root: seccrypto
ms.assetid: 09afc06f-95e8-4519-b0c7-36da5986e077
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: CCertRequest object [Security],GetRequestIdString method, GetRequestIdString, GetRequestIdString method [Security], GetRequestIdString method [Security],CCertRequest object, GetRequestIdString method [Security],ICertRequest3 class, ICertRequest3 class [Security],GetRequestIdString method, ICertRequest3.GetRequestIdString, ICertRequest3::GetRequestIdString, certcli/ICertRequest3::GetRequestIdString, security.icertrequest3_getrequestidstring
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - ICertRequest3.GetRequestIdString
 - CCertRequest.GetRequestIdString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertRequest3::GetRequestIdString


## -description


The <b>GetRequestIdString</b> method gets the current internal request number, formatted as a string, for the request and subsequent certificate.

This can be used to reference a request unambiguously to a server administrator or other interface.


## -parameters




### -param pstrRequestId [out, retval]

A pointer to <b>BSTR</b> variable to receive the request ID string.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns <b>S_OK</b>.

Upon successful completion of this function, the string pointed to by the <i>pstrRequestId</i> parameter is set to the request ID string.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value specifies the current internal request number, as a string, for the request and subsequent certificate.




## -see-also




<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">CCertRequest</a>



<a href="https://msdn.microsoft.com/01de2ac0-4844-41a6-acef-e3e83b350393">ICertRequest3</a>
 

 

