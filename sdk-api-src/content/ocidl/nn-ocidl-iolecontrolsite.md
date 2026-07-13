---
UID: NN:ocidl.IOleControlSite
title: IOleControlSite (ocidl.h)
description: Provides the methods that enable a site object to manage each embedded control within a container.
helpviewer_keywords: ["IOleControlSite","IOleControlSite interface [COM]","IOleControlSite interface [COM]","described","_ctrl_iolecontrolsite","com.iolecontrolsite","ocidl/IOleControlSite"]
old-location: com\iolecontrolsite.htm
tech.root: com
ms.assetid: 8b022f2c-d4b4-44ca-8e69-46e9aa20b3f9
ms.date: 12/05/2018
ms.keywords: IOleControlSite, IOleControlSite interface [COM], IOleControlSite interface [COM],described, _ctrl_iolecontrolsite, com.iolecontrolsite, ocidl/IOleControlSite
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IOleControlSite
 - ocidl/IOleControlSite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleControlSite
---

# IOleControlSite interface


## -description

Provides the methods that enable a site object to manage each embedded control within a container. A site object provides <b>IOleControlSite</b> as well as other site interfaces such as <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a> and <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>. When a control requires the services expressed through this interface, it will query one of the other client site interfaces for <b>IOleControlSite</b>.

## -inheritance

The <b>IOleControlSite</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleControlSite</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iolecontrol">IOleControl</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>
