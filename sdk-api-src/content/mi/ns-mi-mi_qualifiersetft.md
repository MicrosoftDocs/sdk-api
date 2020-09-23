---
UID: NS:mi._MI_QualifierSetFT
title: MI_QualifierSetFT (mi.h)
description: A support structure used in the MI_QualifierSet structure. Use the functions with the name prefix &quot;MI_QualifierSet_&quot; to manipulate these structures.
helpviewer_keywords: ["MI_QualifierSetFT","MI_QualifierSetFT structure [Windows Management Infrastructure (MI)]","mi/MI_QualifierSetFT","wmi_v2.mi_qualifiersetft"]
old-location: wmi_v2\mi_qualifiersetft.htm
tech.root: wmi_v2
ms.assetid: 3868c336-e3c1-4977-8c5d-3964c93b6074
ms.date: 12/05/2018
ms.keywords: MI_QualifierSetFT, MI_QualifierSetFT structure [Windows Management Infrastructure (MI)], mi/MI_QualifierSetFT, wmi_v2.mi_qualifiersetft
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
req.typenames: MI_QualifierSetFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_QualifierSetFT
 - mi/_MI_QualifierSetFT
 - MI_QualifierSetFT
 - mi/MI_QualifierSetFT
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
 - MI_QualifierSetFT
---

## -description

A support structure used in the 
     <a href="/windows/desktop/api/mi/ns-mi-mi_qualifierset">MI_QualifierSet</a> structure. Use the functions with the 
     name prefix "MI_QualifierSet_" to manipulate these structures.

## -struct-fields

### -field GetQualifier

Gets a named qualifier. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_qualifierset_getqualifier">MI_QualifierSet_GetQualifier</a>.

### -field GetQualifierAt

Gets a qualifier at the specified index. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_qualifierset_getqualifierat">MI_QualifierSet_GetQualifierAt</a>.

### -field GetQualifierCount

Gets the number of qualifiers in a qualifier set. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_qualifierset_getqualifiercount">MI_QualifierSet_GetQualifierCount</a>.
