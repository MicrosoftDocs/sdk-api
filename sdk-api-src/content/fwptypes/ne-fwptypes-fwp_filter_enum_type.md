---
UID: NE:fwptypes.FWP_FILTER_ENUM_TYPE_
title: FWP_FILTER_ENUM_TYPE (fwptypes.h)
description: Specifies how the filter enum conditions should be interpreted.
helpviewer_keywords: ["FWP_FILTER_ENUM_FULLY_CONTAINED","FWP_FILTER_ENUM_OVERLAPPING","FWP_FILTER_ENUM_TYPE","FWP_FILTER_ENUM_TYPE enumeration [Filtering]","FWP_FILTER_ENUM_TYPE_MAX","fwp.fwp_filter_enum_type_enum","fwptypes/FWP_FILTER_ENUM_FULLY_CONTAINED","fwptypes/FWP_FILTER_ENUM_OVERLAPPING","fwptypes/FWP_FILTER_ENUM_TYPE","fwptypes/FWP_FILTER_ENUM_TYPE_MAX"]
old-location: fwp\fwp_filter_enum_type_enum.htm
tech.root: fwp
ms.assetid: 842ddac3-52d0-4c29-9db3-8534a0c84659
ms.date: 12/05/2018
ms.keywords: FWP_FILTER_ENUM_FULLY_CONTAINED, FWP_FILTER_ENUM_OVERLAPPING, FWP_FILTER_ENUM_TYPE, FWP_FILTER_ENUM_TYPE enumeration [Filtering], FWP_FILTER_ENUM_TYPE_MAX, fwp.fwp_filter_enum_type_enum, fwptypes/FWP_FILTER_ENUM_FULLY_CONTAINED, fwptypes/FWP_FILTER_ENUM_OVERLAPPING, fwptypes/FWP_FILTER_ENUM_TYPE, fwptypes/FWP_FILTER_ENUM_TYPE_MAX
req.header: fwptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwptypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWP_FILTER_ENUM_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWP_FILTER_ENUM_TYPE_
 - fwptypes/FWP_FILTER_ENUM_TYPE_
 - FWP_FILTER_ENUM_TYPE
 - fwptypes/FWP_FILTER_ENUM_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwptypes.h
api_name:
 - FWP_FILTER_ENUM_TYPE
---

# FWP_FILTER_ENUM_TYPE enumeration


## -description

The <b>FWP_FILTER_ENUM_TYPE</b> enumerated type specifies how the filter enum conditions should be interpreted.

## -enum-fields

### -field FWP_FILTER_ENUM_FULLY_CONTAINED:0

Return only filters that fully contain the enum conditions.

### -field FWP_FILTER_ENUM_OVERLAPPING

Return filters that overlap with the enum conditions, including filters that fully contain the enum conditions.

### -field FWP_FILTER_ENUM_TYPE_MAX

Maximum value for testing purposes.

