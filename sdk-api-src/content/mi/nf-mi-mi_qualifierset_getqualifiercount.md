---
UID: NF:mi.MI_QualifierSet_GetQualifierCount
title: MI_QualifierSet_GetQualifierCount function (mi.h)
description: Gets the number of qualifiers in a qualifier set.
helpviewer_keywords: ["MI_QualifierSet_GetQualifierCount","MI_QualifierSet_GetQualifierCount function [Windows Management Infrastructure (MI)]","mi/MI_QualifierSet_GetQualifierCount","wmi_v2.mi_qualifierset_getqualifiercount"]
old-location: wmi_v2\mi_qualifierset_getqualifiercount.htm
tech.root: wmi_v2
ms.assetid: 0027b8fc-0528-4aa8-85bc-088429e1e045
ms.date: 12/05/2018
ms.keywords: MI_QualifierSet_GetQualifierCount, MI_QualifierSet_GetQualifierCount function [Windows Management Infrastructure (MI)], mi/MI_QualifierSet_GetQualifierCount, wmi_v2.mi_qualifierset_getqualifiercount
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
 - MI_QualifierSet_GetQualifierCount
 - mi/MI_QualifierSet_GetQualifierCount
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
 - MI_QualifierSet_GetQualifierCount
---

# MI_QualifierSet_GetQualifierCount function


## -description

Gets the number of qualifiers in a qualifier set.

## -parameters

### -param self [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_qualifierset">MI_QualifierSet</a> structure.

### -param count [out]

Returned number of qualifiers.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.