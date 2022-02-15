---
UID: NN:shobjidl_core.IProfferService
title: IProfferService (shobjidl_core.h)
description: Exposes a general mechanism for objects to offer services to other objects on the same host.
helpviewer_keywords: ["IProfferService","IProfferService interface [Windows Shell]","IProfferService interface [Windows Shell]","described","inet_IProfferService","shell.IProfferService","shobjidl_core/IProfferService"]
old-location: shell\IProfferService.htm
tech.root: shell
ms.assetid: 91aa5f9a-c276-4822-93e1-9cd2c48ddd9f
ms.date: 12/05/2018
ms.keywords: IProfferService, IProfferService interface [Windows Shell], IProfferService interface [Windows Shell],described, inet_IProfferService, shell.IProfferService, shobjidl_core/IProfferService
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IProfferService
 - shobjidl_core/IProfferService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IProfferService
---

# IProfferService interface


## -description

Exposes a general mechanism for objects to offer services to other objects on the same host.

## -inheritance

The <b>IProfferService</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProfferService</b> also has these types of members:

## -remarks

Objects that expose a service first call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on their host for this interface, then execute <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iprofferservice-profferservice">IProfferService::ProfferService</a>.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iobjectwithsite">IObjectWithSite</a>
