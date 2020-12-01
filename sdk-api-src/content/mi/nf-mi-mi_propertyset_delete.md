---
UID: NF:mi.MI_PropertySet_Delete
title: MI_PropertySet_Delete function (mi.h)
description: Deletes the specified property list that was constructed on the heap.
helpviewer_keywords: ["MI_PropertySet_Delete","MI_PropertySet_Delete function [Windows Management Infrastructure (MI)]","mi/MI_PropertySet_Delete","wmi_v2.mi_propertyset_delete"]
old-location: wmi_v2\mi_propertyset_delete.htm
tech.root: wmi_v2
ms.assetid: 8ab75a67-0b0e-443b-87b1-ca33f44dde9b
ms.date: 12/05/2018
ms.keywords: MI_PropertySet_Delete, MI_PropertySet_Delete function [Windows Management Infrastructure (MI)], mi/MI_PropertySet_Delete, wmi_v2.mi_propertyset_delete
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
 - MI_PropertySet_Delete
 - mi/MI_PropertySet_Delete
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
 - MI_PropertySet_Delete
---

# MI_PropertySet_Delete function


## -description

Deletes the specified property list that was constructed on the heap.

## -parameters

### -param self [in, out]

Property list to be deleted.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.