---
UID: NF:mi.MI_Utilities_MapErrorToMiErrorCategory
title: MI_Utilities_MapErrorToMiErrorCategory function (mi.h)
description: Maps an operating system specific error code to an error category.
helpviewer_keywords: ["MI_RESULT_TYPE_HRESULT","MI_RESULT_TYPE_MI","MI_RESULT_TYPE_WIN32","MI_Utilities_MapErrorToMiErrorCategory","MI_Utilities_MapErrorToMiErrorCategory function [Windows Management Infrastructure (MI)]","mi/MI_Utilities_MapErrorToMiErrorCategory","wmi_v2.mi_utilities_maperrortomierrorcategory"]
old-location: wmi_v2\mi_utilities_maperrortomierrorcategory.htm
tech.root: wmi_v2
ms.assetid: 58ac8e3e-ae87-40b1-bf27-1b32168a033e
ms.date: 12/05/2018
ms.keywords: MI_RESULT_TYPE_HRESULT, MI_RESULT_TYPE_MI, MI_RESULT_TYPE_WIN32, MI_Utilities_MapErrorToMiErrorCategory, MI_Utilities_MapErrorToMiErrorCategory function [Windows Management Infrastructure (MI)], mi/MI_Utilities_MapErrorToMiErrorCategory, wmi_v2.mi_utilities_maperrortomierrorcategory
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
 - MI_Utilities_MapErrorToMiErrorCategory
 - mi/MI_Utilities_MapErrorToMiErrorCategory
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
 - MI_Utilities_MapErrorToMiErrorCategory
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

An <a href="/windows/desktop/api/mi/ne-mi-mi_errorcategory">MI_ErrorCategory</a> structure that indicates the category of error.

## -see-also

<a href="/windows/desktop/api/mi/ne-mi-mi_errorcategory">MI_ErrorCategory</a>