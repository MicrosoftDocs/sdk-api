---
UID: NF:certcli.ICertRequest.GetDispositionMessage
title: ICertRequest::GetDispositionMessage
author: windows-sdk-content
description: Gets a human-readable message that gives the current disposition of the certificate request.
old-location: security\icertrequest2_getdispositionmessage.htm
tech.root: seccrypto
ms.assetid: c3639cf6-c70f-4f15-a0ed-e60abe2955cb
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CCertRequest object [Security],GetDispositionMessage method, GetDispositionMessage, GetDispositionMessage method [Security], GetDispositionMessage method [Security],CCertRequest object, GetDispositionMessage method [Security],ICertRequest interface, GetDispositionMessage method [Security],ICertRequest2 interface, GetDispositionMessage method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetDispositionMessage method, ICertRequest.GetDispositionMessage, ICertRequest2 interface [Security],GetDispositionMessage method, ICertRequest2::GetDispositionMessage, ICertRequest3 interface [Security],GetDispositionMessage method, ICertRequest3::GetDispositionMessage, ICertRequest::GetDispositionMessage, certcli/ICertRequest2::GetDispositionMessage, certcli/ICertRequest3::GetDispositionMessage, certcli/ICertRequest::GetDispositionMessage, security.icertrequest2_getdispositionmessage
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
 - ICertRequest3.GetDispositionMessage
 - ICertRequest2.GetDispositionMessage
 - ICertRequest.GetDispositionMessage
 - CCertRequest.GetDispositionMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertRequest::GetDispositionMessage


## -description


The <b>GetDispositionMessage</b> method gets a human-readable message that gives the current disposition of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>.

Note that the message returned here may have more detail than the returned error code. For example, 
<a href="https://msdn.microsoft.com/ebe5cfa7-6bfd-4454-9272-64e3b1bf0ae2">ICertRequest3::GetLastStatus</a> may return an <b>HRESULT</b>, while <b>GetDispositionMessage</b> will return a detailed reason that specifies why the request was denied.


## -parameters




### -param pstrDispositionMessage [out]

A pointer to the <b>BSTR</b> that contains the disposition message.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

Upon successful completion of this function, *<i>pstrDispositionMessage</i> is set to the <b>BSTR</b> that contains a human-readable message that gives the current disposition of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrDispositionMessage</i>. When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a string that contains a human-readable message that gives the current disposition of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>.




## -remarks



An application would call this method to obtain the message retrieved from the server by means of an earlier call to 
<a href="https://msdn.microsoft.com/22ae8d39-3f16-4f7d-94a0-aa68b03aaa0b">ICertRequest3::Submit</a> or 
<a href="https://msdn.microsoft.com/07a9ac57-f90e-4c5c-b563-8aebbcf8f42e">ICertRequest3::RetrievePending</a>. Additionally, the message is stored in the Certificate Services database and may be viewed by the Certification Authority MMC snap-in (choose the Request Disposition Message column). If the message contains localized text, it was localized on the server (based on the server's locale).


#### Examples


```cpp
#include <windows.h>
#include <stdio.h>
#include <Certcli.h>

    BSTR    bstrDispMsg = NULL;
    // pCertRequest is previously instantiated ICertRequest object 
    // pointer. Retrieve the disposition message for the 
    // previous request.
    hr = pCertRequest->GetDispositionMessage(&bstrDispMsg);
    if (FAILED(hr))
    {
        printf("Failed GetDispositionMessage [%x]\n", hr);
        goto error;
    }
    else
    {
        // Use the disposition message as needed...
    }

    // Done processing.

error:

    // Free BSTR values.
    if (NULL != bstrCA)
        SysFreeString(bstrCA);

    if (NULL != bstrDispMsg)
        SysFreeString(bstrDispMsg);

```





## -see-also




<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">CCertRequest</a>



<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">ICertRequest</a>



<a href="https://msdn.microsoft.com/8587a682-27a5-4f26-b4bb-7088e4e5d8d3">ICertRequest2</a>



<a href="https://msdn.microsoft.com/01de2ac0-4844-41a6-acef-e3e83b350393">ICertRequest3</a>
 

 

