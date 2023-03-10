---
UID: NS:xamlom.ParentChildRelation
title: ParentChildRelation (xamlom.h)
description: Associates a parent object with a child object.
helpviewer_keywords: ["PParentChildRelation","PParentChildRelation structure pointer","ParentChildRelation","ParentChildRelation structure","xaml_diagnostics.parentchildrelation","xamlom/PParentChildRelation","xamlom/ParentChildRelation"]
old-location: xaml_diagnostics\parentchildrelation.htm
tech.root: xaml_diagnostics
ms.assetid: 49BC909B-2886-4F03-8F4D-60B9126DA236
ms.date: 12/05/2018
ms.keywords: PParentChildRelation, PParentChildRelation structure pointer, ParentChildRelation, ParentChildRelation structure, xaml_diagnostics.parentchildrelation, xamlom/PParentChildRelation, xamlom/ParentChildRelation
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XamlOM.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ParentChildRelation
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ParentChildRelation
 - xamlom/ParentChildRelation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xamlom.h
api_name:
 - ParentChildRelation
---

# ParentChildRelation structure


## -description

Associates a parent object with a child object.

## -struct-fields

### -field Parent

A handle to the parent object.

### -field Child

A handle to the child object.

### -field ChildIndex

The index of <b>Child</b> in the <b>Children</b> collection of <b>Parent</b>.

