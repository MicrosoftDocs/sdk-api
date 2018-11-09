---
UID: NF:certcli.ICertRequest.GetRequestId
title: ICertRequest::GetRequestId
author: windows-sdk-content
description: Gets the current internal request number for the request and subsequent certificate.
old-location: security\icertrequest2_getrequestid.htm
tech.root: seccrypto
ms.assetid: bb808834-7083-4b14-bce7-96b6fef242cc
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CCertRequest object [Security],GetRequestId method, GetRequestId, GetRequestId method [Security], GetRequestId method [Security],CCertRequest object, GetRequestId method [Security],ICertRequest interface, GetRequestId method [Security],ICertRequest2 interface, GetRequestId method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetRequestId method, ICertRequest.GetRequestId, ICertRequest2 interface [Security],GetRequestId method, ICertRequest2::GetRequestId, ICertRequest3 interface [Security],GetRequestId method, ICertRequest3::GetRequestId, ICertRequest::GetRequestId, certcli/ICertRequest2::GetRequestId, certcli/ICertRequest3::GetRequestId, certcli/ICertRequest::GetRequestId, security.icertrequest2_getrequestid
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
 - ICertRequest3.GetRequestId
 - ICertRequest2.GetRequestId
 - ICertRequest.GetRequestId
 - CCertRequest.GetRequestId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertRequest::GetRequestId


## -description


The <b>GetRequestId</b> method gets the current internal request number for the request and subsequent certificate.

This can be used to reference a request unambiguously to a server administrator or other interface.


## -parameters




### -param pRequestId [out]

A pointer to the request ID value.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

Upon successful completion of this function, *<i>pRequestId</i> is set to the value of the request ID.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value specifies the current internal request number for the request and subsequent certificate.




## -see-also




<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">CCertRequest</a>



<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">ICertRequest</a>



<a href="https://msdn.microsoft.com/8587a682-27a5-4f26-b4bb-7088e4e5d8d3">ICertRequest2</a>



<a href="https://msdn.microsoft.com/01de2ac0-4844-41a6-acef-e3e83b350393">ICertRequest3</a>
 

 

