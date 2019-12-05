---
UID: NF:drt.DrtDeleteNullSecurityProvider
title: DrtDeleteNullSecurityProvider function (drt.h)
description: DrtDeleteNullSecurityProvider function deletes a null security provider for a Distributed Routing Table.
old-location: p2p\drtdeletenullsecurityprovider.htm
tech.root: P2PSdk
ms.assetid: 950a43f3-1c1d-4fb3-988b-d58ac9eff2f8
ms.date: 12/05/2018
ms.keywords: DrtDeleteNullSecurityProvider, DrtDeleteNullSecurityProvider function [Distributed Routing Tables], drt/DrtDeleteNullSecurityProvider, p2p.drtdeletenullsecurityprovider
ms.topic: function
f1_keywords:
- drt/DrtDeleteNullSecurityProvider
dev_langs:
- c++
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Drtprov.lib
req.dll: Drt.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- drt.dll
api_name:
- DrtDeleteNullSecurityProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DrtDeleteNullSecurityProvider function


## -description


The <b>DrtDeleteNullSecurityProvider</b> function deletes a null security provider for a Distributed Routing Table.


## -parameters




### -param pSecurityProvider [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/drt/ns-drt-drt_security_provider">DRT_SECURITY_PROVIDER</a> structure specifying the security provider to delete.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/drt/ns-drt-drt_security_provider">DRT_SECURITY_PROVIDER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider">DrtCreateNullSecurityProvider</a>
 

 

