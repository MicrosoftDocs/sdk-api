---
UID: NE:uxtheme.PROPERTYORIGIN
title: PROPERTYORIGIN (uxtheme.h)
description: Returned by GetThemePropertyOrigin to specify where a property was found.
helpviewer_keywords: ["PO_CLASS","PO_GLOBAL","PO_NOTFOUND","PO_PART","PO_STATE","PROPERTYORIGIN","PROPERTYORIGIN enumeration [Windows Controls]","controls.PROPERTYORIGIN","controls.inet_PROPERTYORIGIN","inet_PROPERTYORIGIN","inet_PROPERTYORIGIN_cpp","uxtheme/PO_CLASS","uxtheme/PO_GLOBAL","uxtheme/PO_NOTFOUND","uxtheme/PO_PART","uxtheme/PO_STATE","uxtheme/PROPERTYORIGIN"]
old-location: controls\PROPERTYORIGIN.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\enums\propertyorigin.htm
ms.date: 12/05/2018
ms.keywords: PO_CLASS, PO_GLOBAL, PO_NOTFOUND, PO_PART, PO_STATE, PROPERTYORIGIN, PROPERTYORIGIN enumeration [Windows Controls], controls.PROPERTYORIGIN, controls.inet_PROPERTYORIGIN, inet_PROPERTYORIGIN, inet_PROPERTYORIGIN_cpp, uxtheme/PO_CLASS, uxtheme/PO_GLOBAL, uxtheme/PO_NOTFOUND, uxtheme/PO_PART, uxtheme/PO_STATE, uxtheme/PROPERTYORIGIN
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - PROPERTYORIGIN
 - uxtheme/PROPERTYORIGIN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uxtheme.h
api_name:
 - PROPERTYORIGIN
---

# PROPERTYORIGIN enumeration


## -description

Returned by <a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemepropertyorigin">GetThemePropertyOrigin</a> to specify where a property was found.

## -enum-fields

### -field PO_STATE

Property was found in the state section.

### -field PO_PART

Property was found in the part section.

### -field PO_CLASS

Property was found in the class section.

### -field PO_GLOBAL

Property was found in the list of global variables.

### -field PO_NOTFOUND

Property was not found.

## -see-also

<a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemepropertyorigin">GetThemePropertyOrigin</a>