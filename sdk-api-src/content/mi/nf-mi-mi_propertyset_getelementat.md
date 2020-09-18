---
UID: NF:mi.MI_PropertySet_GetElementAt
title: MI_PropertySet_GetElementAt function (mi.h)
description: Gets the element of a property set at the specified index.
helpviewer_keywords: ["MI_PropertySet_GetElementAt","MI_PropertySet_GetElementAt function [Windows Management Infrastructure (MI)]","mi/MI_PropertySet_GetElementAt","wmi_v2.mi_propertyset_getelementat"]
old-location: wmi_v2\mi_propertyset_getelementat.htm
tech.root: wmi_v2
ms.assetid: 234fe69f-cba6-4ad0-b970-f90346488417
ms.date: 12/05/2018
ms.keywords: MI_PropertySet_GetElementAt, MI_PropertySet_GetElementAt function [Windows Management Infrastructure (MI)], mi/MI_PropertySet_GetElementAt, wmi_v2.mi_propertyset_getelementat
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_PropertySet_GetElementAt
 - mi/MI_PropertySet_GetElementAt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_PropertySet_GetElementAt
---

# MI_PropertySet_GetElementAt function


## -description

Gets the element of a property set at the specified index.

## -parameters

### -param self [in]

Property list from which to get the element.

### -param index

Zero-based index where the element exists in the property set.

### -param name

Returned element name. The lifetime of this value is the same as the property list.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.