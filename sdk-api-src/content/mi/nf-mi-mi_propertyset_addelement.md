---
UID: NF:mi.MI_PropertySet_AddElement
title: MI_PropertySet_AddElement function (mi.h)
description: Adds a name to the property list.
helpviewer_keywords: ["MI_PropertySet_AddElement","MI_PropertySet_AddElement function [Windows Management Infrastructure (MI)]","mi/MI_PropertySet_AddElement","wmi_v2.mi_propertyset_addelement"]
old-location: wmi_v2\mi_propertyset_addelement.htm
tech.root: wmi_v2
ms.assetid: b7676ebd-bc65-4aad-b3c7-263ceb976b20
ms.date: 12/05/2018
ms.keywords: MI_PropertySet_AddElement, MI_PropertySet_AddElement function [Windows Management Infrastructure (MI)], mi/MI_PropertySet_AddElement, wmi_v2.mi_propertyset_addelement
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
 - MI_PropertySet_AddElement
 - mi/MI_PropertySet_AddElement
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
 - MI_PropertySet_AddElement
---

# MI_PropertySet_AddElement function


## -description

Adds a name to the property list.

## -parameters

### -param self [in, out]

The property list to which to add the name.

### -param name

A null-terminated string that represents the name to add to the property list.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.