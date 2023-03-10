---
UID: NN:sbtsv.ITsSbResourceNotification
title: ITsSbResourceNotification (sbtsv.h)
description: Exposes methods that Remote Desktop Connection Broker (RD Connection Broker) uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects. (ITsSbResourceNotification)
helpviewer_keywords: ["ITsSbResourceNotification","ITsSbResourceNotification interface [Remote Desktop Services]","ITsSbResourceNotification interface [Remote Desktop Services]","described","sbtsv/ITsSbResourceNotification","termserv.itssbresourcenotification"]
old-location: termserv\itssbresourcenotification.htm
tech.root: TermServ
ms.assetid: 70785b82-239d-4957-9703-ced685a2e0b8
ms.date: 12/05/2018
ms.keywords: ITsSbResourceNotification, ITsSbResourceNotification interface [Remote Desktop Services], ITsSbResourceNotification interface [Remote Desktop Services],described, sbtsv/ITsSbResourceNotification, termserv.itssbresourcenotification
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
 - ITsSbResourceNotification
 - sbtsv/ITsSbResourceNotification
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
 - ITsSbResourceNotification
---

# ITsSbResourceNotification interface


## -description

Exposes methods that Remote Desktop Connection Broker (RD Connection Broker) uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects. Plug-ins can use these notifications in many ways. For example, they can implement load-balancing algorithms.

## -inheritance

The <b>ITsSbResourceNotification</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITsSbResourceNotification</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex">ITsSbResourceNotificationEx</a>



<a href="/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
