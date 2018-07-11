---
UID: NF:xenroll.IEnroll4.addAttributeToRequestWStr
title: IEnroll4::addAttributeToRequestWStr
author: windows-sdk-content
description: Adds an attribute to the certificate request.
old-location: security\ienroll4_addattributetorequestwstr.htm
old-project: seccrypto
ms.assetid: 71421bca-ef72-47d3-8f4a-95cb9768644f
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IEnroll4 interface [Security],addAttributeToRequestWStr method, IEnroll4.addAttributeToRequestWStr, IEnroll4::addAttributeToRequestWStr, addAttributeToRequestWStr, addAttributeToRequestWStr method [Security], addAttributeToRequestWStr method [Security],IEnroll4 interface, security.ienroll4_addattributetorequestwstr, xenroll/IEnroll4::addAttributeToRequestWStr
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
 - IEnroll4.addAttributeToRequestWStr
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll4::addAttributeToRequestWStr


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addAttributeToRequestWStr</b> method adds an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a> to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters




### -param Flags [in]

This parameter is reserved for future use and must be set to zero.


### -param pwszName [in]

A pointer to a null-terminated wide character string that represents the object identifier (OID) for the attribute name.


### -param pblobValue [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that represents the attribute value.


## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

