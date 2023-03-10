---
UID: NN:sbtsv.ITsSbProvider
title: ITsSbProvider (sbtsv.h)
description: Exposes methods that create default implementations of objects that are used in Remote Desktop Virtualization.
helpviewer_keywords: ["ITsSbProvider","ITsSbProvider interface [Remote Desktop Services]","ITsSbProvider interface [Remote Desktop Services]","described","sbtsv/ITsSbProvider","termserv.itssbprovider"]
old-location: termserv\itssbprovider.htm
tech.root: TermServ
ms.assetid: a8574750-d86e-4b0d-a534-d005596e2a33
ms.date: 12/05/2018
ms.keywords: ITsSbProvider, ITsSbProvider interface [Remote Desktop Services], ITsSbProvider interface [Remote Desktop Services],described, sbtsv/ITsSbProvider, termserv.itssbprovider
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
 - ITsSbProvider
 - sbtsv/ITsSbProvider
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
 - ITsSbProvider
---

# ITsSbProvider interface


## -description

Exposes methods that create default implementations of objects that are used in Remote Desktop Virtualization.

The  <b>ITsSbProvider</b> interface is a helper interface, aimed at reducing the amount of code that the plug-in 
implementer needs to write. It provides a default implementation of some objects, such as 
environment, target, and session objects.

## -inheritance

The <b>ITsSbProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITsSbProvider</b> also has these types of members:

## -see-also

<a href="/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
