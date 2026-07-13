---
UID: NF:drt.DrtDeleteDnsBootstrapResolver
title: DrtDeleteDnsBootstrapResolver function (drt.h)
description: DrtDeleteDnsBootstrapResolver function deletes a DNS Bootstrap Provider instance.
helpviewer_keywords: ["DrtDeleteDnsBootstrapResolver","DrtDeleteDnsBootstrapResolver function [Distributed Routing Tables]","drt/DrtDeleteDnsBootstrapResolver","p2p.drtdeletednsbootstrapresolver"]
old-location: p2p\drtdeletednsbootstrapresolver.htm
tech.root: p2p
ms.assetid: fc3d0b6a-1bf3-41f9-82b6-965c285bc6c7
ms.date: 12/05/2018
ms.keywords: DrtDeleteDnsBootstrapResolver, DrtDeleteDnsBootstrapResolver function [Distributed Routing Tables], drt/DrtDeleteDnsBootstrapResolver, p2p.drtdeletednsbootstrapresolver
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
 - DrtDeleteDnsBootstrapResolver
 - drt/DrtDeleteDnsBootstrapResolver
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
 - DrtDeleteDnsBootstrapResolver
---

# DrtDeleteDnsBootstrapResolver function


## -description

The <b>DrtDeleteDnsBootstrapResolver</b> function deletes a DNS Bootstrap Provider instance.

## -parameters

### -param pResolver [in]

Pointer to a DRT_BOOTSTRAP_PROVIDER instance specifying the security provider to delete.

## -see-also

<a href="/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider">DRT_BOOTSTRAP_PROVIDER</a>



<a href="/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver">DrtCreateDnsBootstrapResolver</a>