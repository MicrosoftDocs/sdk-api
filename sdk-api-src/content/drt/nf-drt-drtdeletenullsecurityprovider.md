---
UID: NF:drt.DrtDeleteNullSecurityProvider
title: DrtDeleteNullSecurityProvider function (drt.h)
description: DrtDeleteNullSecurityProvider function deletes a null security provider for a Distributed Routing Table.
helpviewer_keywords: ["DrtDeleteNullSecurityProvider","DrtDeleteNullSecurityProvider function [Distributed Routing Tables]","drt/DrtDeleteNullSecurityProvider","p2p.drtdeletenullsecurityprovider"]
old-location: p2p\drtdeletenullsecurityprovider.htm
tech.root: p2p
ms.assetid: 950a43f3-1c1d-4fb3-988b-d58ac9eff2f8
ms.date: 12/05/2018
ms.keywords: DrtDeleteNullSecurityProvider, DrtDeleteNullSecurityProvider function [Distributed Routing Tables], drt/DrtDeleteNullSecurityProvider, p2p.drtdeletenullsecurityprovider
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrtDeleteNullSecurityProvider
 - drt/DrtDeleteNullSecurityProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtDeleteNullSecurityProvider
---

# DrtDeleteNullSecurityProvider function


## -description

The <b>DrtDeleteNullSecurityProvider</b> function deletes a null security provider for a Distributed Routing Table.

## -parameters

### -param pSecurityProvider [in]

Pointer to a <a href="/windows/desktop/api/drt/ns-drt-drt_security_provider">DRT_SECURITY_PROVIDER</a> structure specifying the security provider to delete.

## -see-also

<a href="/windows/desktop/api/drt/ns-drt-drt_security_provider">DRT_SECURITY_PROVIDER</a>



<a href="/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider">DrtCreateNullSecurityProvider</a>