---
UID: NF:drt.DrtDeleteDerivedKeySecurityProvider
title: DrtDeleteDerivedKeySecurityProvider function (drt.h)
description: DrtDeleteDerivedKeySecurityProvider function deletes a derived key security provider for a Distributed Routing Table.
helpviewer_keywords: ["DrtDeleteDerivedKeySecurityProvider","DrtDeleteDerivedKeySecurityProvider function [Peer Networking]","drt/DrtDeleteDerivedKeySecurityProvider","p2p.drtdeletederivedkeysecurityprovider"]
old-location: p2p\drtdeletederivedkeysecurityprovider.htm
tech.root: p2p
ms.assetid: 89b2bbe6-51a3-48fc-85c9-13e1b0cfd880
ms.date: 12/05/2018
ms.keywords: DrtDeleteDerivedKeySecurityProvider, DrtDeleteDerivedKeySecurityProvider function [Peer Networking], drt/DrtDeleteDerivedKeySecurityProvider, p2p.drtdeletederivedkeysecurityprovider
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
 - DrtDeleteDerivedKeySecurityProvider
 - drt/DrtDeleteDerivedKeySecurityProvider
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
 - DrtDeleteDerivedKeySecurityProvider
---

# DrtDeleteDerivedKeySecurityProvider function


## -description

The <b>DrtDeleteDerivedKeySecurityProvider</b> function deletes a derived key security provider for a Distributed Routing Table.

## -parameters

### -param pSecurityProvider [in]

Pointer to a <a href="/windows/desktop/api/drt/ns-drt-drt_security_provider">DRT_SECURITY_PROVIDER</a> specifying the security provider to delete.

## -see-also

<a href="/windows/desktop/api/drt/nf-drt-drtcreatederivedkey">DrtCreateDerivedKey</a>



<a href="/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider">DrtCreateDerivedKeySecurityProvider</a>