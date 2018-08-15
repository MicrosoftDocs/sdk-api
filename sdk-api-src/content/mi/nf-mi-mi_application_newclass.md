---
UID: NF:mi.MI_Application_NewClass
title: MI_Application_NewClass function
author: windows-sdk-content
description: Creates an MI_Class from an MI_ClassDecl structure.
old-location: wmi_v2\mi_application_newclass.htm
old-project: wmi_v2
ms.assetid: f325532e-8e29-40d4-ab7f-52f318ae9349
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_Application_NewClass, MI_Application_NewClass function [Windows Management Infrastructure (MI)], mi/MI_Application_NewClass, wmi_v2.mi_application_newclass
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MI_Type
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mi.dll
api_name:
 - MI_Application_NewClass
product: Windows
targetos: Windows
req.lib: Mi.lib
req.dll: Mi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MI_Application_NewClass function


## -description


Creates an <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> from an 
    <a href="https://msdn.microsoft.com/8e2e2838-5d08-4e51-be96-0928042ccb9f">MI_ClassDecl</a> structure. The resulting 
    <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> structure must be closed by using the 
    <a href="https://msdn.microsoft.com/a2794f8f-a69a-49f3-8d7e-512c80ea782b">MI_Class_Delete</a> function.


## -parameters




### -param application [in]

Handle returned from 
      <a href="https://msdn.microsoft.com/32696A33-820D-4D01-AF71-DDA1F34EFBE0">MI_Application_Initialize</a>.


### -param classDecl [in]

The <a href="https://msdn.microsoft.com/8e2e2838-5d08-4e51-be96-0928042ccb9f">MI_ClassDecl</a> for the class to create.


### -param namespaceName [in, optional]

The optional namespace name.


### -param serverName [in, optional]

The optional server name.


### -param classObject [out]

The resultant <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> structure.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the 
      function return code. This can be one of the following codes.



