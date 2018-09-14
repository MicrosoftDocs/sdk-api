---
UID: NF:xenroll.IEnroll.createFilePKCS10WStr
title: IEnroll::createFilePKCS10WStr
author: windows-sdk-content
description: Creates a base64-encoded PKCS #10 certificate request and saves it in a file.
old-location: security\ienroll4_createfilepkcs10wstr.htm
tech.root: seccrypto
ms.assetid: 5edd54c5-9dfb-44b8-a293-4fe6a8de45e3
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IEnroll interface [Security],createFilePKCS10WStr method, IEnroll.createFilePKCS10WStr, IEnroll::createFilePKCS10WStr, createFilePKCS10WStr, createFilePKCS10WStr method [Security], createFilePKCS10WStr method [Security],IEnroll interface, security.ienroll4_createfilepkcs10wstr, xenroll/IEnroll::createFilePKCS10WStr
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
 - IEnroll.createFilePKCS10WStr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::createFilePKCS10WStr


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createFilePKCS10WStr</b> method creates a base64-encoded PKCS #10 <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a> and saves it in a file. This method was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This method differs from 
the <a href="https://msdn.microsoft.com/ebbcc9ad-9f87-4abe-963b-38c57a60e45e">createPKCS10WStr</a> method only in saving the base64-encoded PKCS #10 certificate request  to the file specified by the <i>wszPKCS10FileName</i> parameter.


## -parameters




### -param DNName [in]

The distinguished name (DN) of the entity for which the request is being made. <i>DNName</i> must follow the <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.500</a> naming convention. For example, "CN=User, O=Microsoft". If a two-letter prefix does not exist, an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) may be provided instead.


### -param Usage [in]

An <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">OID</a> that describes the purpose of the certificate being generated, for example, individual or commercial Authenticode certificate, or client authentication. You can also specify multiple OIDs separated by a comma.

The OID is passed through to the PKCS #10 request. The control does not examine the OID.


### -param wszPKCS10FileName [in]

The name of the file in which the base64-encoded PKCS #10 is saved. The contents of this file may be submitted to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> for processing.


## -remarks



By default, the Microsoft Base Cryptographic Provider is used, and a unique signature key is created.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

