---
UID: NN:oleidl.IOleItemContainer
title: IOleItemContainer (oleidl.h)
description: Used by item monikers when they are bound to the objects they identify.
helpviewer_keywords: ["IOleItemContainer","IOleItemContainer interface [COM]","IOleItemContainer interface [COM]","described","_com_ioleitemcontainer","com.ioleitemcontainer","oleidl/IOleItemContainer"]
old-location: com\ioleitemcontainer.htm
tech.root: com
ms.assetid: fe306a36-da24-4b1e-ab42-359d37962d36
ms.date: 12/05/2018
ms.keywords: IOleItemContainer, IOleItemContainer interface [COM], IOleItemContainer interface [COM],described, _com_ioleitemcontainer, com.ioleitemcontainer, oleidl/IOleItemContainer
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.idl
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
 - IOleItemContainer
 - oleidl/IOleItemContainer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleItemContainer
---

# IOleItemContainer interface


## -description

Used by item monikers when they are bound to the objects they identify. 


When any container of objects uses item monikers to identify its objects, it must define a naming scheme for those objects. The container's <b>IOleItemContainer</b> implementation uses knowledge of that naming scheme to retrieve an object given a particular name. Item monikers use the container's <b>IOleItemContainer</b> implementation during binding. 



This interface is not supported for use across machine boundaries.

## -inheritance

The <b>IOleItemContainer</b> interface inherits from <b>IOleContainer</b>. <b>IOleItemContainer</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-createitemmoniker">CreateItemMoniker</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>
