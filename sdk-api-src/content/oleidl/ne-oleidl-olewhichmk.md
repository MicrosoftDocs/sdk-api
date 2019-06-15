---
UID: NE:oleidl.tagOLEWHICHMK
title: OLEWHICHMK (oleidl.h)
author: windows-sdk-content
description: Indicates which part of an object's moniker is being set or retrieved.
old-location: com\olewhichmk.htm
tech.root: com
ms.assetid: 3774c868-c312-4e7c-aa57-cdb13000a87c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OLEWHICHMK, OLEWHICHMK enumeration [COM], OLEWHICHMK_CONTAINER, OLEWHICHMK_OBJFULL, OLEWHICHMK_OBJREL, _ole_OLEWHICHMK, com.olewhichmk, oleidl/OLEWHICHMK, oleidl/OLEWHICHMK_CONTAINER, oleidl/OLEWHICHMK_OBJFULL, oleidl/OLEWHICHMK_OBJREL
ms.topic: enum
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleIdl.h
api_name:
 - OLEWHICHMK
product: Windows
targetos: Windows
req.typenames: OLEWHICHMK
req.redist: 
ms.custom: 19H1
---

# OLEWHICHMK enumeration


## -description


Indicates which part of an object's moniker is being set or retrieved.


## -enum-fields




### -field OLEWHICHMK_CONTAINER

The moniker of the object's container. Typically, this is a file moniker. This moniker is not persistently stored inside the object, since the container can be renamed even while the object is not loaded.


### -field OLEWHICHMK_OBJREL

The moniker of the object relative to its container. Typically, this is an item moniker, and it is part of the persistent state of the object. If this moniker is composed on to the end of the container's moniker, the resulting moniker is the full moniker of the object.


### -field OLEWHICHMK_OBJFULL

The full moniker of the object. Binding to this moniker results in a connection to the object. This moniker is not persistently stored inside the object, since the container can be renamed even while the object is not loaded.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getmoniker">IOleClientSite::GetMoniker</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getmoniker">IOleObject::GetMoniker</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setmoniker">IOleObject::SetMoniker</a>
 

 

