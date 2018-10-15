---
UID: NF:xenroll.ICEnroll4.acceptFileResponse
title: ICEnroll4::acceptFileResponse
author: windows-sdk-content
description: Accepts delivery of the credentials issued in response to an earlier call to createFileRequest, and it places the credentials in the appropriate store.
old-location: security\icenroll4_acceptfileresponse.htm
tech.root: seccrypto
ms.assetid: 127863ca-843b-46c5-b375-fb0400e8b49b
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CEnroll object [Security],acceptFileResponse method, ICEnroll4 interface [Security],acceptFileResponse method, ICEnroll4.acceptFileResponse, ICEnroll4::acceptFileResponse, _xen_icenroll4_acceptfileresponse, acceptFileResponse, acceptFileResponse method [Security], acceptFileResponse method [Security],CEnroll object, acceptFileResponse method [Security],ICEnroll4 interface, security.icenroll4_acceptfileresponse, xenroll/ICEnroll4::acceptFileResponse
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
 - ICEnroll4.acceptFileResponse
 - CEnroll.acceptFileResponse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll4::acceptFileResponse


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>acceptFileResponse</b> method accepts delivery of the credentials issued in response to an earlier call to 
<a href="https://msdn.microsoft.com/8902eb8e-c597-42a6-8836-6a24181da4d4">createFileRequest</a>, and it places the credentials in the appropriate store. This method was first defined in the <a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a> interface.

The response may be a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">PKCS #7</a> message or a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Management over CMS</a> (CMC) response.


## -parameters




### -param strResponseFileName [in]

Specifies the name of the file that contains the base64-encoded response.


## -returns



<h3>VB</h3>
If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The response named in the <i>strResponseFileName</i> parameter must contain exactly one certificate; a child certificate cannot be present.

The response may be either a PKCS #7 or a full CMC response; however, to accept a full CMC response, the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> must support <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding of CMC structures.

When this method is called from script, the method displays a user interface that asks whether the user will allow installation of a  certificate and whether the user will allow a read operation from the file system.



