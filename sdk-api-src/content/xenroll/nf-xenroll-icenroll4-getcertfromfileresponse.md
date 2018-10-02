---
UID: NF:xenroll.ICEnroll4.getCertFromFileResponse
title: ICEnroll4::getCertFromFileResponse
author: windows-sdk-content
description: Retrieves the certificate from a file containing a response from a certification authority. This method was first defined in the ICEnroll4 interface.
old-location: security\icenroll4_getcertfromfileresponse.htm
tech.root: seccrypto
ms.assetid: 0e89465b-4525-4b36-b0c7-7f34dc4a34aa
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CEnroll object [Security],getCertFromFileResponse method, ICEnroll4 interface [Security],getCertFromFileResponse method, ICEnroll4.getCertFromFileResponse, ICEnroll4::getCertFromFileResponse, _xen_icenroll4_getcertfromfileresponse, getCertFromFileResponse, getCertFromFileResponse method [Security], getCertFromFileResponse method [Security],CEnroll object, getCertFromFileResponse method [Security],ICEnroll4 interface, security.icenroll4_getcertfromfileresponse, xenroll/ICEnroll4::getCertFromFileResponse
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xenroll.h
req.include-header: 
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.getCertFromFileResponse
 - CEnroll.getCertFromFileResponse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll4::getCertFromFileResponse


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>getCertFromFileResponse</b> method retrieves the certificate from a file containing a response from a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a>.
			 This method was first defined in the <a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a> interface.


## -parameters




### -param strResponseFileName [in]

Specifies the name of the file that contains the response.


### -param pstrCert [out]

A pointer to a <b>BSTR</b> value that receives the certificate retrieved from the response. When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a <b>String</b> that contains a certificate.




## -remarks



The response contained in <i>strResponseFileName</i> must contain exactly one certificate; a child certificate cannot be present.

The response may be either a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">PKCS #7</a> or a full <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Management over CMS</a> (CMC) response. However, to accept a full CMC response, the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) must support <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding of CMC structures.

When this method is called from script, the method displays a user interface that asks whether the user will allow a read operation from the file system.



