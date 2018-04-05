---
UID: NF:xenroll.IEnroll4.addNameValuePairToRequestWStr
title: IEnroll4::addNameValuePairToRequestWStr method
author: windows-driver-content
description: Adds an unauthenticated name-value string pair to the request.
old-location: security\ienroll4_addnamevaluepairtorequestwstr.htm
old-project: SecCrypto
ms.assetid: 25f8ae01-e975-4ada-b17c-c97385dc0585
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IEnroll4, IEnroll4 interface [Security], addNameValuePairToRequestWStr method, IEnroll4::addNameValuePairToRequestWStr, addNameValuePairToRequestWStr method [Security], addNameValuePairToRequestWStr method [Security], IEnroll4 interface, addNameValuePairToRequestWStr,IEnroll4.addNameValuePairToRequestWStr, security.ienroll4_addnamevaluepairtorequestwstr, xenroll/IEnroll4::addNameValuePairToRequestWStr
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
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Xenroll.dll
api_name:
-	IEnroll4.addNameValuePairToRequestWStr
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll4::addNameValuePairToRequestWStr method


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addNameValuePairToRequestWStr</b> method adds an unauthenticated name-value string pair to the request. This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters




### -param Flags [in]

This parameter is reserved for future use and must be set to zero.


### -param pwszName [in]

A pointer to a null-terminated wide character string that represents the name portion of the name-value pair.


### -param pwszValue [in]

A pointer to a null-terminated wide character string that represents the value portion of the name-value pair.


## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

