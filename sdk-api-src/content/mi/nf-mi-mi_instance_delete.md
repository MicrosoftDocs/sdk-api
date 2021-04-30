---
UID: NF:mi.MI_Instance_Delete
title: MI_Instance_Delete function (mi.h)
description: Deletes an instance that was created on the heap or cloned from another instance.
helpviewer_keywords: ["MI_Instance_Delete","MI_Instance_Delete function [Windows Management Infrastructure (MI)]","mi/MI_Instance_Delete","wmi_v2.mi_instance_delete"]
old-location: wmi_v2\mi_instance_delete.htm
tech.root: wmi_v2
ms.assetid: 6370e464-b262-4c91-a3c8-889911df7965
ms.date: 12/05/2018
ms.keywords: MI_Instance_Delete, MI_Instance_Delete function [Windows Management Infrastructure (MI)], mi/MI_Instance_Delete, wmi_v2.mi_instance_delete
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
 - MI_Instance_Delete
 - mi/MI_Instance_Delete
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
 - MI_Instance_Delete
---

# MI_Instance_Delete function


## -description

Deletes an instance that was created on the heap or cloned from another instance.

## -parameters

### -param self [in, out]

Instance to be released.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

Instances created with the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_clone">MI_Instance_Clone</a>, <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newinstance">MI_Application_NewInstance</a>, <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_newinstance">MI_Context_NewInstance</a>, <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_newdynamicinstance">MI_Context_NewDynamicInstance</a>, <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_newparameters">MI_Context_NewParameters</a>, and <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_utilities_cimerrorfromerrorcode">MI_Utilities_CimErrorFromErrorCode</a> functions should be passed to this function when they are no longer required.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newinstance">MI_Application_NewInstance</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_newdynamicinstance">MI_Context_NewDynamicInstance</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_newinstance">MI_Context_NewInstance</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_newparameters">MI_Context_NewParameters</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_clone">MI_Instance_Clone</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_utilities_cimerrorfromerrorcode">MI_Utilities_CimErrorFromErrorCode</a>