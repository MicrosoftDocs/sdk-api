---
UID: NF:mi.MI_Application_NewInstanceFromClass
title: MI_Application_NewInstanceFromClass function (mi.h)
description: Creates a new MI_Instance object based on a class object.
helpviewer_keywords: ["MI_Application_NewInstanceFromClass","MI_Application_NewInstanceFromClass function [Windows Management Infrastructure (MI)]","mi/MI_Application_NewInstanceFromClass","wmi_v2.mi_application_newinstancefromclass"]
old-location: wmi_v2\mi_application_newinstancefromclass.htm
tech.root: wmi_v2
ms.assetid: 57d1ec84-79b7-40f3-be3b-1b5b57a9d5b3
ms.date: 12/05/2018
ms.keywords: MI_Application_NewInstanceFromClass, MI_Application_NewInstanceFromClass function [Windows Management Infrastructure (MI)], mi/MI_Application_NewInstanceFromClass, wmi_v2.mi_application_newinstancefromclass
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
 - MI_Application_NewInstanceFromClass
 - mi/MI_Application_NewInstanceFromClass
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
 - MI_Application_NewInstanceFromClass
---

# MI_Application_NewInstanceFromClass function


## -description

Creates a new <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> object based on a class object.

## -parameters

### -param application [in]

A pointer to a handle returned from a call to the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_initializev1">MI_Application_Initialize</a> function.

### -param className

A null-terminated string that represents the class name for the instance being created.

### -param classObject [in, optional]

A pointer to the class object from which to create an instance.

### -param instance

A pointer to the instance returned from this function call.

## -returns

This function returns MI_INLINE MI_Result.