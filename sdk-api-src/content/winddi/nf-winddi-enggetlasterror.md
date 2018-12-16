---
UID: NF:winddi.EngGetLastError
title: EngGetLastError function
author: windows-sdk-content
description: The EngGetLastError function returns the last error code logged by GDI for the calling thread.
old-location: display\enggetlasterror.htm
tech.root: display
ms.assetid: 47138077-125e-4da9-b0de-e437a9b1733d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EngGetLastError, EngGetLastError function [Display Devices], display.enggetlasterror, gdifncs_19c92fa6-2204-40e7-adc5-22a85b9ba0d5.xml, winddi/EngGetLastError
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngGetLastError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngGetLastError function


## -description


The <b>EngGetLastError</b> function returns the last error code logged by GDI for the calling thread.


## -parameters






## -returns



The return value is the last error code set by <b>EngSetLastError</b>.




## -remarks



<b>EngGetLastError</b> facilitates communication of GDI and/or driver error conditions to an application.




## -see-also




<a href="https://msdn.microsoft.com/8887eed8-c60d-4217-92bf-f770be071c49">EngSetLastError</a>
 

 

