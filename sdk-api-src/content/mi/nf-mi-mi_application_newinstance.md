---
UID: NF:mi.MI_Application_NewInstance
title: MI_Application_NewInstance function (mi.h)
description: Creates a new MI_Instance object to be passed to various MI operation APIs that require instances.
helpviewer_keywords: ["MI_Application_NewInstance","MI_Application_NewInstance function [Windows Management Infrastructure (MI)]","mi/MI_Application_NewInstance","wmi_v2.mi_application_newinstance"]
old-location: wmi_v2\mi_application_newinstance.htm
tech.root: wmi_v2
ms.assetid: e46adc55-c5dc-4395-b746-2ff13cc1e4bb
ms.date: 12/05/2018
ms.keywords: MI_Application_NewInstance, MI_Application_NewInstance function [Windows Management Infrastructure (MI)], mi/MI_Application_NewInstance, wmi_v2.mi_application_newinstance
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
 - MI_Application_NewInstance
 - mi/MI_Application_NewInstance
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
 - MI_Application_NewInstance
---

# MI_Application_NewInstance function


## -description

Creates a new <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> object to be passed to various MI operation APIs that require instances.

## -parameters

### -param application [in]

A pointer to a handle returned from a call to the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_initializev1">MI_Application_Initialize</a> function.

### -param className

The class name for the instance being created.

### -param classRTTI [in, optional]

A pointer to optional run time type information for the object being created.

### -param instance

A pointer to the instance returned from this function call.

## -returns

This function returns MI_INLINE MI_Result.

## -remarks

When you have finished using the instance created by this call, delete it by calling the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_delete">MI_Instance_Delete</a> function.