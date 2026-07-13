---
UID: NN:sbtsv.ITsSbResourceNotificationEx
title: ITsSbResourceNotificationEx (sbtsv.h)
description: Exposes methods that Remote Desktop Connection Broker (RD Connection Broker) uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects. (ITsSbResourceNotificationEx)
helpviewer_keywords: ["ITsSbResourceNotificationEx","ITsSbResourceNotificationEx interface [Remote Desktop Services]","ITsSbResourceNotificationEx interface [Remote Desktop Services]","described","sbtsv/ITsSbResourceNotificationEx","termserv.itssbresourcenotificationex"]
old-location: termserv\itssbresourcenotificationex.htm
tech.root: TermServ
ms.assetid: 5e40535d-62b2-4d16-a995-61c24aefb2e5
ms.date: 12/05/2018
ms.keywords: ITsSbResourceNotificationEx, ITsSbResourceNotificationEx interface [Remote Desktop Services], ITsSbResourceNotificationEx interface [Remote Desktop Services],described, sbtsv/ITsSbResourceNotificationEx, termserv.itssbresourcenotificationex
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
 - ITsSbResourceNotificationEx
 - sbtsv/ITsSbResourceNotificationEx
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
 - ITsSbResourceNotificationEx
---

# ITsSbResourceNotificationEx interface


## -description

Exposes methods that Remote Desktop Connection Broker (RD Connection Broker) uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects. Plug-ins can use these notifications in many ways. For example, they can implement load-balancing algorithms.

## -inheritance

The <b>ITsSbResourceNotificationEx</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITsSbResourceNotificationEx</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification">ITsSbResourceNotification</a>



<a href="/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
