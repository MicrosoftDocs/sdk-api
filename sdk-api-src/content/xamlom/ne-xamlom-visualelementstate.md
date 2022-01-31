---
UID: NE:xamlom.VisualElementState
title: VisualElementState (xamlom.h)
description: Defines constants that specify the state of an element in the visual tree.
helpviewer_keywords: ["ErrorInvalidResource","ErrorResolved","ErrorResourceNotFound","VisualElementState","VisualElementState enumeration","xaml_diagnostics.visualelementstate","xamlom/ErrorInvalidResource","xamlom/ErrorResolved","xamlom/ErrorResourceNotFound","xamlom/VisualElementState"]
old-location: xaml_diagnostics\visualelementstate.htm
tech.root: xaml_diagnostics
ms.assetid: 6D2AA4D0-4EB6-419F-AA9F-1B2404E0ED42
ms.date: 12/05/2018
ms.keywords: ErrorInvalidResource, ErrorResolved, ErrorResourceNotFound, VisualElementState, VisualElementState enumeration, xaml_diagnostics.visualelementstate, xamlom/ErrorInvalidResource, xamlom/ErrorResolved, xamlom/ErrorResourceNotFound, xamlom/VisualElementState
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
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
req.typenames: VisualElementState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VisualElementState
 - xamlom/VisualElementState
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
 - VisualElementState
---

# VisualElementState enumeration


## -description

Defines constants that specify the state of an element in the visual tree.

## -enum-fields

### -field ErrorResolved:0

The error has been fixed.

### -field ErrorResourceNotFound

The resource could not be resolved.

### -field ErrorInvalidResource

The resource was found, but does not match the property.

## -see-also

<a href="/previous-versions/windows/desktop/xaml_diagnostics/ivisualtreeservicecallback2-onelementstatechanged">OnElementStateChanged</a>
