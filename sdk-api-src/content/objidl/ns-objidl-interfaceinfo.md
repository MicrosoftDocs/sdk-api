---
UID: NS:objidl.tagINTERFACEINFO
title: INTERFACEINFO (objidl.h)
description: Contains information about incoming calls.
helpviewer_keywords: ["*LPINTERFACEINFO","INTERFACEINFO","INTERFACEINFO structure [COM]","LPINTERFACEINFO","LPINTERFACEINFO structure pointer [COM]","_com_INTERFACEINFO","com.interfaceinfo","objidl/INTERFACEINFO","objidl/LPINTERFACEINFO"]
old-location: com\interfaceinfo.htm
tech.root: com
ms.assetid: 5c2c07bf-1c15-4f21-baef-103837ea24d0
ms.date: 12/05/2018
ms.keywords: '*LPINTERFACEINFO, INTERFACEINFO, INTERFACEINFO structure [COM], LPINTERFACEINFO, LPINTERFACEINFO structure pointer [COM], _com_INTERFACEINFO, com.interfaceinfo, objidl/INTERFACEINFO, objidl/LPINTERFACEINFO'
req.header: objidl.h
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
targetos: Windows
req.typenames: INTERFACEINFO, *LPINTERFACEINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagINTERFACEINFO
 - objidl/tagINTERFACEINFO
 - LPINTERFACEINFO
 - objidl/LPINTERFACEINFO
 - INTERFACEINFO
 - objidl/INTERFACEINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - INTERFACEINFO
---

# INTERFACEINFO structure


## -description

Contains information about incoming calls.

## -struct-fields

### -field pUnk

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the object.

### -field iid

The identifier of the requested interface.

### -field wMethod

The interface method.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imessagefilter-handleincomingcall">IMessageFilter::HandleInComingCall</a>