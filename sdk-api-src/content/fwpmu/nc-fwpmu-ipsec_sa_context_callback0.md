---
UID: NC:fwpmu.IPSEC_SA_CONTEXT_CALLBACK0
title: IPSEC_SA_CONTEXT_CALLBACK0 (fwpmu.h)
description: Is used to add custom behavior to the IPsec security association (SA) context subscription process.
helpviewer_keywords: ["IPSEC_SA_CONTEXT_CALLBACK0","IPSEC_SA_CONTEXT_CALLBACK0 callback","IPSEC_SA_CONTEXT_CALLBACK0 callback function [Filtering]","fwp.ipsec_sa_context_callback0","fwpmu/IPSEC_SA_CONTEXT_CALLBACK0"]
old-location: fwp\ipsec_sa_context_callback0.htm
tech.root: fwp
ms.assetid: a4515d39-8566-4418-a6be-687f4f7d9969
ms.date: 12/05/2018
ms.keywords: IPSEC_SA_CONTEXT_CALLBACK0, IPSEC_SA_CONTEXT_CALLBACK0 callback, IPSEC_SA_CONTEXT_CALLBACK0 callback function [Filtering], fwp.ipsec_sa_context_callback0, fwpmu/IPSEC_SA_CONTEXT_CALLBACK0
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_SA_CONTEXT_CALLBACK0
 - fwpmu/IPSEC_SA_CONTEXT_CALLBACK0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - fwpmu.h
api_name:
 - IPSEC_SA_CONTEXT_CALLBACK0
---

## -description

The <b>IPSEC_SA_CONTEXT_CALLBACK0</b> function is used to add custom behavior to the IPsec security association (SA) context subscription process.

## -parameters

### -param context [in, out]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="/windows/win32/api/fwpmu/nf-fwpmu-ipsecsacontextsubscribe0">IPsecSaContextSubscribe0</a> function.

### -param change [in]

Type: **const [IPSEC_SA_CONTEXT_CHANGE0](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)\***

The IPsec SA context information.

## -remarks

Call <a href="/windows/win32/api/fwpmu/nf-fwpmu-ipsecsacontextsubscribe0">IPsecSaContextSubscribe0</a> to register this callback function.

## -see-also

<a href="/windows/win32/api/fwpmu/nf-fwpmu-ipsecsacontextsubscribe0">IPsecSaContextSubscribe0</a>
