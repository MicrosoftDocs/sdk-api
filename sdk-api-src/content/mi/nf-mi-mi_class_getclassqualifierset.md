---
UID: NF:mi.MI_Class_GetClassQualifierSet
title: MI_Class_GetClassQualifierSet function (mi.h)
description: Gets the qualifier set that is associated with the specified class object.
helpviewer_keywords: ["MI_Class_GetClassQualifierSet","MI_Class_GetClassQualifierSet function [Windows Management Infrastructure (MI)]","mi/MI_Class_GetClassQualifierSet","wmi_v2.mi_class_getclassqualifierset"]
old-location: wmi_v2\mi_class_getclassqualifierset.htm
tech.root: wmi_v2
ms.assetid: 900ae879-a728-43a9-8dcb-de20a50f8dce
ms.date: 12/05/2018
ms.keywords: MI_Class_GetClassQualifierSet, MI_Class_GetClassQualifierSet function [Windows Management Infrastructure (MI)], mi/MI_Class_GetClassQualifierSet, wmi_v2.mi_class_getclassqualifierset
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
 - MI_Class_GetClassQualifierSet
 - mi/MI_Class_GetClassQualifierSet
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
 - MI_Class_GetClassQualifierSet
---

# MI_Class_GetClassQualifierSet function


## -description

Gets the qualifier set that is associated with the specified class object.

## -parameters

### -param self [in]

A pointer to the class from which to get the qualifier set.

### -param qualifierSet [out, optional]

A pointer to the variable to receive the returned class qualifier set.  This parameter is optional. The memory associated with the qualifier set is valid until the class object is deleted. When you have finished using the class qualifier set, delete the class object by calling the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_delete">MI_Class_Delete</a> function.

## -returns

This function returns MI_INLINE MI_Result.