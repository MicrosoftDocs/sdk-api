---
UID: NS:imepad.tagAPPLETIDLIST
title: APPLETIDLIST (imepad.h)
description: Specifies an IImePadApplet IID list.
helpviewer_keywords: ["*LPAPPLETIDLIST","APPLETIDLIST","APPLETIDLIST structure [Internationalization for Windows Applications]","PAPPLETIDLIST","PAPPLETIDLIST structure pointer [Internationalization for Windows Applications]","imepad/APPLETIDLIST","imepad/PAPPLETIDLIST","intl.appletidlist"]
old-location: intl\appletidlist.htm
tech.root: Intl
ms.assetid: 6A93B726-1C35-4779-AF60-859DF3B18462
ms.date: 12/05/2018
ms.keywords: '*LPAPPLETIDLIST, APPLETIDLIST, APPLETIDLIST structure [Internationalization for Windows Applications], PAPPLETIDLIST, PAPPLETIDLIST structure pointer [Internationalization for Windows Applications], imepad/APPLETIDLIST, imepad/PAPPLETIDLIST, intl.appletidlist'
req.header: imepad.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: APPLETIDLIST, *LPAPPLETIDLIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAPPLETIDLIST
 - imepad/tagAPPLETIDLIST
 - LPAPPLETIDLIST
 - imepad/LPAPPLETIDLIST
 - APPLETIDLIST
 - imepad/APPLETIDLIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Imepad.h
api_name:
 - APPLETIDLIST
---

# APPLETIDLIST structure


## -description

Specifies an <a href="/windows/desktop/api/imepad/nn-imepad-iimepadapplet">IImePadApplet</a> IID list.

## -struct-fields

### -field count

The number of the IID's implemented in this applet.

### -field pIIDList

The IID list. This must be allocated with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>.