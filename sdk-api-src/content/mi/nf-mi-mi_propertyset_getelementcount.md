---
UID: NF:mi.MI_PropertySet_GetElementCount
title: MI_PropertySet_GetElementCount function (mi.h)
description: Gets the number of elements in the specified property set.
helpviewer_keywords: ["MI_PropertySet_GetElementCount","MI_PropertySet_GetElementCount function [Windows Management Infrastructure (MI)]","mi/MI_PropertySet_GetElementCount","wmi_v2.mi_propertyset_getelementcount"]
old-location: wmi_v2\mi_propertyset_getelementcount.htm
tech.root: wmi_v2
ms.assetid: 450f778c-6b59-4c01-9c21-7f96f28ebe26
ms.date: 12/05/2018
ms.keywords: MI_PropertySet_GetElementCount, MI_PropertySet_GetElementCount function [Windows Management Infrastructure (MI)], mi/MI_PropertySet_GetElementCount, wmi_v2.mi_propertyset_getelementcount
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
 - MI_PropertySet_GetElementCount
 - mi/MI_PropertySet_GetElementCount
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
 - MI_PropertySet_GetElementCount
---

# MI_PropertySet_GetElementCount function


## -description

Gets the number of elements in the specified property set.

## -parameters

### -param self [in]

Property set to enumerate.

### -param count [out]

Returned number of element in the property set.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.