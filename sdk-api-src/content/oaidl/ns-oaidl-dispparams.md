---
UID: NS:oaidl.tagDISPPARAMS
title: DISPPARAMS (oaidl.h)
description: Contains the arguments passed to a method or property.
helpviewer_keywords: ["DISPPARAMS","DISPPARAMS structure [Automation]","_oa96_DISPPARAMS","automat.dispparams","oaidl/DISPPARAMS"]
old-location: automat\dispparams.htm
tech.root: automat
ms.assetid: a16e5a21-766e-4287-b039-13429aa78f8b
ms.date: 12/05/2018
ms.keywords: DISPPARAMS, DISPPARAMS structure [Automation], _oa96_DISPPARAMS, automat.dispparams, oaidl/DISPPARAMS
req.header: oaidl.h
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
req.typenames: DISPPARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDISPPARAMS
 - oaidl/tagDISPPARAMS
 - DISPPARAMS
 - oaidl/DISPPARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OaIdl.h
api_name:
 - DISPPARAMS
---

# DISPPARAMS structure


## -description

Contains the arguments passed to a method or property.

## -struct-fields

### -field rgvarg

An array of arguments.

**Note**: these arguments appear in reverse order

### -field rgdispidNamedArgs

The dispatch IDs of the named arguments.

### -field cArgs

The number of arguments.

### -field cNamedArgs

The number of named arguments.

