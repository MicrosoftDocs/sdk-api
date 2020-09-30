---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Specifies the type of DirectWrite factory object.
helpviewer_keywords: ["DWRITE_FACTORY_TYPE","DWRITE_FACTORY_TYPE enumeration [Direct Write]","DWRITE_FACTORY_TYPE_ISOLATED","DWRITE_FACTORY_TYPE_SHARED","directwrite.dwrite_factory_type","dwrite/DWRITE_FACTORY_TYPE","dwrite/DWRITE_FACTORY_TYPE_ISOLATED","dwrite/DWRITE_FACTORY_TYPE_SHARED"]
old-location: directwrite\dwrite_factory_type.htm
tech.root: DirectWrite
ms.assetid: ce51d8cd-3125-49e3-878c-9d4b446e2422
ms.date: 12/05/2018
ms.keywords: DWRITE_FACTORY_TYPE, DWRITE_FACTORY_TYPE enumeration [Direct Write], DWRITE_FACTORY_TYPE_ISOLATED, DWRITE_FACTORY_TYPE_SHARED, directwrite.dwrite_factory_type, dwrite/DWRITE_FACTORY_TYPE, dwrite/DWRITE_FACTORY_TYPE_ISOLATED, dwrite/DWRITE_FACTORY_TYPE_SHARED
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - DWRITE_FACTORY_TYPE
 - dwrite/DWRITE_FACTORY_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_FACTORY_TYPE
---

# DWRITE_FACTORY_TYPE enumeration


## -description

Specifies the type of DirectWrite factory object.

## -enum-fields

### -field DWRITE_FACTORY_TYPE_SHARED

Indicates that the DirectWrite factory is a shared factory and that it allows for the reuse of cached font data across multiple in-process components. Such factories also take advantage of cross process font caching components for better performance.

### -field DWRITE_FACTORY_TYPE_ISOLATED

Indicates that the DirectWrite factory object is isolated. Objects created from the isolated factory do not interact with internal DirectWrite state from other components.

## -remarks

A DirectWrite factory object contains information about its internal state, such as font loader registration and cached font data. In most cases you should use the shared factory object, because it allows multiple components that use DirectWrite to share internal DirectWrite state information, thereby reducing memory usage. However, there are cases when it is desirable to reduce the impact of a component on the rest of the process, such as a plug-in from an untrusted source,  by sandboxing and isolating it from the rest of the process components. In such cases, you should use an isolated factory for the sandboxed component.

