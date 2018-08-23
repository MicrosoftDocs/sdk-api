---
UID: NF:certenroll.IX509SCEPEnrollment.CreateRequestMessage
title: IX509SCEPEnrollment::CreateRequestMessage
author: windows-sdk-content
description: Create a PKCS10 request message with a challenge password. The request message is in an enveloped PKCS7 encrypted with the SCEP server encryption certificate and signed by the server signing certificate.
old-location: security\ix509scepenrollment_createrequestmessage.htm
old-project: seccertenroll
ms.assetid: b86d6dc3-aa96-45f3-9551-f24c39ea6cbf
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateRequestMessage, CreateRequestMessage method [Security], CreateRequestMessage method [Security],IX509SCEPEnrollment interface, IX509SCEPEnrollment interface [Security],CreateRequestMessage method, IX509SCEPEnrollment.CreateRequestMessage, IX509SCEPEnrollment::CreateRequestMessage, certenroll/IX509SCEPEnrollment::CreateRequestMessage, security.ix509scepenrollment_createrequestmessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - IX509SCEPEnrollment.CreateRequestMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: Certenroll.dll
req.irql: 
---

# IX509SCEPEnrollment::CreateRequestMessage


## -description


Create a PKCS10 request message with a challenge password. The request message is in an enveloped PKCS7 encrypted with the SCEP server encryption certificate and signed by the server signing certificate.


## -parameters




### -param Encoding [in]


### -param pValue [out, retval]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You must call the <a href="https://msdn.microsoft.com/dcb887ab-c8b7-42e7-8b49-93755d24ba70">Initialize</a> method before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/fcbac911-9e37-4994-bbb6-544b19a92749">IX509SCEPEnrollment</a>
 

 

