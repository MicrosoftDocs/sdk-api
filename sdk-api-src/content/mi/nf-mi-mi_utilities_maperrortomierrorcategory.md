---
UID: NF:mi.MI_Utilities_MapErrorToMiErrorCategory
title: MI_Utilities_MapErrorToMiErrorCategory function
author: windows-driver-content
description: Maps an operating system specific error code to an error category.
old-location: wmi_v2\mi_utilities_maperrortomierrorcategory.htm
old-project: wmi_v2
ms.assetid: 58ac8e3e-ae87-40b1-bf27-1b32168a033e
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: MI_RESULT_TYPE_HRESULT, MI_RESULT_TYPE_MI, MI_RESULT_TYPE_WIN32, MI_Utilities_MapErrorToMiErrorCategory, MI_Utilities_MapErrorToMiErrorCategory function [Windows Management Infrastructure (MI)], mi/MI_Utilities_MapErrorToMiErrorCategory, wmi_v2.mi_utilities_maperrortomierrorcategory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_Utilities_MapErrorToMiErrorCategory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Utilities_MapErrorToMiErrorCategory function


## -description


Maps an operating system specific error code to an error category.


## -parameters




### -param errorType

A null-terminated string representing an error type. Use one of these constants.



#### MI_RESULT_TYPE_MI

MI result type



#### MI_RESULT_TYPE_HRESULT

HRESULT (COM return type) result type



#### MI_RESULT_TYPE_WIN32

Win32 result type


### -param error

Error code to map.


## -returns



An <a href="https://msdn.microsoft.com/afcc85a1-5aaf-41df-8cd7-b88739b73cf9">MI_ErrorCategory</a> structure that indicates the category of error.




## -see-also




<a href="https://msdn.microsoft.com/afcc85a1-5aaf-41df-8cd7-b88739b73cf9">MI_ErrorCategory</a>
 

 

