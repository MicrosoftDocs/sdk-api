---
UID: NN:sbtsv.ITsSbGlobalStore
title: ITsSbGlobalStore (sbtsv.h)
description: Exposes methods that query for target computers, sessions, environments, and farms that have been added to the Remote Desktop Connection Broker (RD Connection Broker) store.
helpviewer_keywords: ["ITsSbGlobalStore","ITsSbGlobalStore interface [Remote Desktop Services]","ITsSbGlobalStore interface [Remote Desktop Services]","described","sbtsv/ITsSbGlobalStore","termserv.itssbglobalstore"]
old-location: termserv\itssbglobalstore.htm
tech.root: TermServ
ms.assetid: d25b6f73-ee5f-40e4-9c49-fd48dd3990d2
ms.date: 12/05/2018
ms.keywords: ITsSbGlobalStore, ITsSbGlobalStore interface [Remote Desktop Services], ITsSbGlobalStore interface [Remote Desktop Services],described, sbtsv/ITsSbGlobalStore, termserv.itssbglobalstore
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - ITsSbGlobalStore
 - sbtsv/ITsSbGlobalStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbGlobalStore
---

# ITsSbGlobalStore interface


## -description

Exposes methods that query for target computers, sessions, environments, and farms that have been added 
to the Remote Desktop Connection Broker (RD Connection Broker) store. Plug-ins can obtain an instance of the global store from the <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider">ITsSbProvider</a> 
object that they retrieve during initialization.

## -inheritance

The <b>ITsSbGlobalStore</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITsSbGlobalStore</b> also has these types of members:

## -see-also

<a href="/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
