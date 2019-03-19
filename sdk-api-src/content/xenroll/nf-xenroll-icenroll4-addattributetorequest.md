---
UID: NF:xenroll.ICEnroll4.addAttributeToRequest
title: ICEnroll4::addAttributeToRequest (xenroll.h)
author: windows-sdk-content
description: Adds an attribute to the certificate request. This method was first defined in the ICEnroll4 interface.
old-location: security\icenroll4_addattributetorequest.htm
tech.root: SecCrypto
ms.assetid: a15fe06c-e2a5-4292-ad82-ea350e652a07
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CEnroll object [Security],addAttributeToRequest method, ICEnroll4 interface [Security],addAttributeToRequest method, ICEnroll4.addAttributeToRequest, ICEnroll4::addAttributeToRequest, _xen_icenroll4_addattributetorequest, addAttributeToRequest, addAttributeToRequest method [Security], addAttributeToRequest method [Security],CEnroll object, addAttributeToRequest method [Security],ICEnroll4 interface, security.icenroll4_addattributetorequest, xenroll/ICEnroll4::addAttributeToRequest
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
 - ICEnroll4.addAttributeToRequest
 - CEnroll.addAttributeToRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll4::addAttributeToRequest


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addAttributeToRequest</b> method adds an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a> to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>.  This method was first defined in the <a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a> interface.


## -parameters




### -param Flags [in]

This parameter is reserved for future use and must be set to zero.


### -param strName [in]

An <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) that represents the attribute name.


### -param strValue [in]

A base64-encoded or binary attribute value.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



