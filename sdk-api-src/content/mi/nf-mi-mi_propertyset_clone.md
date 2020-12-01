---
UID: NF:mi.MI_PropertySet_Clone
title: MI_PropertySet_Clone function (mi.h)
description: Creates a copy of the specified property set on the heap.
helpviewer_keywords: ["MI_PropertySet_Clone","MI_PropertySet_Clone function [Windows Management Infrastructure (MI)]","mi/MI_PropertySet_Clone","wmi_v2.mi_propertyset_clone"]
old-location: wmi_v2\mi_propertyset_clone.htm
tech.root: wmi_v2
ms.assetid: 77e7fc5c-3fb9-4037-94b9-c93155c06416
ms.date: 12/05/2018
ms.keywords: MI_PropertySet_Clone, MI_PropertySet_Clone function [Windows Management Infrastructure (MI)], mi/MI_PropertySet_Clone, wmi_v2.mi_propertyset_clone
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
 - MI_PropertySet_Clone
 - mi/MI_PropertySet_Clone
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
 - MI_PropertySet_Clone
---

# MI_PropertySet_Clone function


## -description

Creates a copy of the specified property set on the heap.

## -parameters

### -param self [in]

Property set to be cloned.

### -param newPropertySet

The returned property set clone. This clone will eventually need to be deleted by using the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_propertyset_delete">MI_PropertySet_Delete</a> function.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

The <i>newPropertySet</i> clone should be passed eventually to the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_propertyset_delete">MI_PropertySet_Delete</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_propertyset_delete">MI_PropertySet_Delete</a>