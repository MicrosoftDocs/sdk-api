---
UID: NF:mi.MI_QualifierSet_GetQualifier
title: MI_QualifierSet_GetQualifier function (mi.h)
description: Gets the qualifier information based on the given qualifier name.
helpviewer_keywords: ["MI_QualifierSet_GetQualifier","MI_QualifierSet_GetQualifier function [Windows Management Infrastructure (MI)]","mi/MI_QualifierSet_GetQualifier","wmi_v2.mi_qualifierset_getqualifier"]
old-location: wmi_v2\mi_qualifierset_getqualifier.htm
tech.root: wmi_v2
ms.assetid: 16dde421-3746-4722-9f08-56835b7603fb
ms.date: 12/05/2018
ms.keywords: MI_QualifierSet_GetQualifier, MI_QualifierSet_GetQualifier function [Windows Management Infrastructure (MI)], mi/MI_QualifierSet_GetQualifier, wmi_v2.mi_qualifierset_getqualifier
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
 - MI_QualifierSet_GetQualifier
 - mi/MI_QualifierSet_GetQualifier
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
 - MI_QualifierSet_GetQualifier
---

# MI_QualifierSet_GetQualifier function


## -description

Gets the qualifier information based on the given qualifier name.

## -parameters

### -param self [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_qualifierset">MI_QualifierSet</a> structure.

### -param name

A null-terminated string that represents the name of the qualifier to get.

### -param qualifierType [out]

Returned qualifier type.

### -param qualifierFlags [out]

Returned qualifier flags that indicate the scope of a qualifier.

### -param qualifierValue [out]

Returned qualifier value. This value has the lifetime of the qualifier set.

### -param index [out]

Returned zero-based index of the qualifier.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.