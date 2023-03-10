---
UID: NF:mi.MI_PropertySet_ContainsElement
title: MI_PropertySet_ContainsElement function (mi.h)
description: Determines whether the property list contains the specified property name.
helpviewer_keywords: ["MI_PropertySet_ContainsElement","MI_PropertySet_ContainsElement function [Windows Management Infrastructure (MI)]","mi/MI_PropertySet_ContainsElement","wmi_v2.mi_propertyset_containselement"]
old-location: wmi_v2\mi_propertyset_containselement.htm
tech.root: wmi_v2
ms.assetid: 71cf9c53-4e97-432c-9dfe-bef8ba119f71
ms.date: 12/05/2018
ms.keywords: MI_PropertySet_ContainsElement, MI_PropertySet_ContainsElement function [Windows Management Infrastructure (MI)], mi/MI_PropertySet_ContainsElement, wmi_v2.mi_propertyset_containselement
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
 - MI_PropertySet_ContainsElement
 - mi/MI_PropertySet_ContainsElement
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
 - MI_PropertySet_ContainsElement
---

# MI_PropertySet_ContainsElement function


## -description

Determines whether the property list contains the specified property name.

## -parameters

### -param self [in]

Property list to be checked.

### -param name

A null-terminated string that represents the name to check for in the property list.

### -param flag [out]

Returned Boolean value. <b>MI_TRUE</b> indicates that the specified property was found; otherwise <b>MI_FALSE</b> is returned.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.