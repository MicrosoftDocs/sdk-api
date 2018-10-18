---
UID: NC:wincrypt.PFN_CERT_CREATE_CONTEXT_SORT_FUNC
title: PFN_CERT_CREATE_CONTEXT_SORT_FUNC
author: windows-sdk-content
description: Called for each sorted context entry when a context is created.
old-location: security\pfn_cert_create_context_sort_func.htm
tech.root: seccrypto
ms.assetid: 5ad79970-d076-4e97-bf56-d6aad4b46eaa
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: PFN_CERT_CREATE_CONTEXT_SORT_FUNC, PFN_CERT_CREATE_CONTEXT_SORT_FUNC callback, PFN_CERT_CREATE_CONTEXT_SORT_FUNC callback function [Security], security.pfn_cert_create_context_sort_func, wincrypt/PFN_CERT_CREATE_CONTEXT_SORT_FUNC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CERT_CREATE_CONTEXT_SORT_FUNC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CERT_CREATE_CONTEXT_SORT_FUNC callback function


## -description


The <b>PFN_CERT_CREATE_CONTEXT_SORT_FUNC</b> callback function is called for each sorted context entry when a context is created. This function pointer is passed in the <b>pfnSort</b> member of the <a href="https://msdn.microsoft.com/1486cb60-56f0-4ce4-b283-6f92dcbbea26">CERT_CREATE_CONTEXT_PARA</a> structure.


## -parameters




### -param cbTotalEncoded [in]

The total number of bytes of the encoded entries.


### -param cbRemainEncoded [in]

The number of bytes remaining to be encoded.


### -param cEntry [in]

The current number of sorted entries.


### -param *pvSort [in, out]

An application-defined value that is passed in the <b>pvSort</b> member of the <a href="https://msdn.microsoft.com/1486cb60-56f0-4ce4-b283-6f92dcbbea26">CERT_CREATE_CONTEXT_PARA</a> structure.


## -returns



Return <b>TRUE</b> to continue the sort or <b>FALSE</b> to stop the sort. If <b>FALSE</b> is returned, <a href="https://msdn.microsoft.com/0911054b-a47a-4046-b121-a236fc4b018b">CertCreateContext</a> will fail and set the last error code to <b>ERROR_CANCELLED</b>.




## -see-also




<a href="https://msdn.microsoft.com/1486cb60-56f0-4ce4-b283-6f92dcbbea26">CERT_CREATE_CONTEXT_PARA</a>



<a href="https://msdn.microsoft.com/0911054b-a47a-4046-b121-a236fc4b018b">CertCreateContext</a>
 

 

