---
UID: NF:xenroll.IEnroll4.addBlobPropertyToCertificateWStr
title: IEnroll4::addBlobPropertyToCertificateWStr
author: windows-sdk-content
description: The IEnroll4::addBlobPropertyToCertificateWStr method adds a BLOB property to a certificate.
old-location: security\ienroll4_addblobpropertytocertificatewstr.htm
old-project: SecCrypto
ms.assetid: 954c1b2f-08ea-471c-902f-1aa5523d58b3
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IEnroll4 interface [Security],addBlobPropertyToCertificateWStr method, IEnroll4.addBlobPropertyToCertificateWStr, IEnroll4::addBlobPropertyToCertificateWStr, addBlobPropertyToCertificateWStr, addBlobPropertyToCertificateWStr method [Security], addBlobPropertyToCertificateWStr method [Security],IEnroll4 interface, security.ienroll4_addblobpropertytocertificatewstr, xenroll/IEnroll4::addBlobPropertyToCertificateWStr
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll4.addBlobPropertyToCertificateWStr
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll4::addBlobPropertyToCertificateWStr


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addBlobPropertyToCertificateWStr</b> method adds a <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> property to a certificate. This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters




### -param lPropertyId [in]

The identifier of the BLOB property to add to the certificate.


### -param lReserved [in]

This parameter is reserved. Must be zero.


### -param pBlobProperty [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that represents the data for  the BLOB property.


## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

