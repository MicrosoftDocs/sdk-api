---
UID: NF:mi.MI_Application_NewClass
title: MI_Application_NewClass function (mi.h)
description: Creates an MI_Class from an MI_ClassDecl structure.
helpviewer_keywords: ["MI_Application_NewClass","MI_Application_NewClass function [Windows Management Infrastructure (MI)]","mi/MI_Application_NewClass","wmi_v2.mi_application_newclass"]
old-location: wmi_v2\mi_application_newclass.htm
tech.root: wmi_v2
ms.assetid: f325532e-8e29-40d4-ab7f-52f318ae9349
ms.date: 12/05/2018
ms.keywords: MI_Application_NewClass, MI_Application_NewClass function [Windows Management Infrastructure (MI)], mi/MI_Application_NewClass, wmi_v2.mi_application_newclass
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mi.lib
req.dll: Mi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MI_Application_NewClass
 - mi/MI_Application_NewClass
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mi.dll
api_name:
 - MI_Application_NewClass
---

# MI_Application_NewClass function


## -description

Creates an <a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> from an 
    <a href="/windows/desktop/api/mi/ns-mi-mi_classdecl">MI_ClassDecl</a> structure. The resulting 
    <a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> structure must be closed by using the 
    <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_delete">MI_Class_Delete</a> function.

## -parameters

### -param application [in]

Handle returned from 
      <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_initializev1">MI_Application_Initialize</a>.

### -param classDecl [in]

The <a href="/windows/desktop/api/mi/ns-mi-mi_classdecl">MI_ClassDecl</a> for the class to create.

### -param namespaceName [in, optional]

The optional namespace name.

### -param serverName [in, optional]

The optional server name.

### -param classObject [out]

The resultant <a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> structure.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the 
      function return code. This can be one of the following codes.