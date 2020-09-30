---
UID: NF:drt.DrtUnregisterKey
title: DrtUnregisterKey function (drt.h)
description: The DrtUnregisterKey function deregisters a key from the DRT.
helpviewer_keywords: ["DrtUnregisterKey","DrtUnregisterKey function [Peer Networking]","drt/DrtUnregisterKey","p2p.drtunregisterkey"]
old-location: p2p\drtunregisterkey.htm
tech.root: p2p
ms.assetid: cf8f877b-44a8-4153-bf02-0b0061bc53d2
ms.date: 12/05/2018
ms.keywords: DrtUnregisterKey, DrtUnregisterKey function [Peer Networking], drt/DrtUnregisterKey, p2p.drtunregisterkey
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
req.lib: Drt.lib
req.dll: Drt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrtUnregisterKey
 - drt/DrtUnregisterKey
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
 - DrtUnregisterKey
---

## -description

The <b>DrtUnregisterKey</b> function deregisters a key from the DRT.

## -parameters

### -param hKeyRegistration [in]

The DRT handle returned by the <a href="/windows/desktop/api/drt/nf-drt-drtregisterkey">DrtRegisterKey</a> function specifying a registered key within the DRT.

## -remarks

A node can deregister a key anytime after registration.  Additionally, if an application calls <a href="/windows/desktop/api/drt/nf-drt-drtclose">DrtClose</a>, all keys are deregistered by the DRT infrastructure.

Only the application that registered they key may deregister it. An application can deregister a key from the local node. Upon completion the function triggers a <b>DRT_EVENT_LEAFSET_KEY_CHANGE</b> event;  informing the application and other nodes participating in the DRT mesh of the deregistration.

## -see-also

<a href="/windows/desktop/api/drt/nf-drt-drtclose">DrtClose</a>



<a href="/windows/desktop/api/drt/nf-drt-drtopen">DrtOpen</a>



<a href="/windows/desktop/api/drt/nf-drt-drtregisterkey">DrtRegisterKey</a>