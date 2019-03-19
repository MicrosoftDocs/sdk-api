---
UID: NC:fwpmu.IPSEC_SA_CONTEXT_CALLBACK0
title: IPSEC_SA_CONTEXT_CALLBACK0 (fwpmu.h)
author: windows-sdk-content
description: Is used to add custom behavior to the IPsec security association (SA) context subscription process.
old-location: fwp\ipsec_sa_context_callback0.htm
tech.root: fwp
ms.assetid: a4515d39-8566-4418-a6be-687f4f7d9969
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPSEC_SA_CONTEXT_CALLBACK0, IPSEC_SA_CONTEXT_CALLBACK0 callback, IPSEC_SA_CONTEXT_CALLBACK0 callback function [Filtering], fwp.ipsec_sa_context_callback0, fwpmu/IPSEC_SA_CONTEXT_CALLBACK0
ms.topic: callback
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - fwpmu.h
api_name:
 - IPSEC_SA_CONTEXT_CALLBACK0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPSEC_SA_CONTEXT_CALLBACK0 callback function


## -description


The <b>IPSEC_SA_CONTEXT_CALLBACK0</b> function is used to add custom behavior to the IPsec security association (SA) context  subscription process.


## -parameters




### -param *context [in, out]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="https://msdn.microsoft.com/dadb22b2-6b20-401f-b2b5-256135a345b1">IPsecSaContextSubscribe0</a> function.


### -param *change [in]

Type: <b>const <a href="https://msdn.microsoft.com/a81df783-72d8-4374-a3f8-44c3491a98db">IPSEC_SA_CONTEXT_CHANGE0</a>*</b>

The IPsec SA context information.


## -returns



This callback function does not return a value.




## -remarks



Call <a href="https://msdn.microsoft.com/dadb22b2-6b20-401f-b2b5-256135a345b1">IPsecSaContextSubscribe0</a> to register this callback function.




## -see-also




<a href="https://msdn.microsoft.com/dadb22b2-6b20-401f-b2b5-256135a345b1">IPsecSaContextSubscribe0</a>
 

 

