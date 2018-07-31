---
UID: NF:xenroll.IEnroll4.removePendingRequestWStr
title: IEnroll4::removePendingRequestWStr
author: windows-sdk-content
description: Removes a pending request from the client's request store.
old-location: security\ienroll4_removependingrequestwstr.htm
old-project: SecCrypto
ms.assetid: 0e00fad2-dc06-421d-9a8c-27c5a951466c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IEnroll4 interface [Security],removePendingRequestWStr method, IEnroll4.removePendingRequestWStr, IEnroll4::removePendingRequestWStr, removePendingRequestWStr, removePendingRequestWStr method [Security], removePendingRequestWStr method [Security],IEnroll4 interface, security.ienroll4_removependingrequestwstr, xenroll/IEnroll4::removePendingRequestWStr
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
 - IEnroll4.removePendingRequestWStr
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll4::removePendingRequestWStr


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>removePendingRequestWStr</b> method removes a pending request from the client's request store.  This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters




### -param thumbPrintBlob [in]


<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that represents the thumbprint, or <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a>, of the certificate data.


## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

