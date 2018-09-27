---
UID: NF:fltuser.FilterCreate
title: FilterCreate function
author: windows-sdk-content
description: The FilterCreate function creates a handle for the given minifilter.
old-location: ifsk\filtercreate.htm
tech.root: ifsk
ms.assetid: 950e0b5b-4ee3-4eed-9039-823a6942cd38
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: FilterCreate, FilterCreate function [Installable File System Drivers], FltWin32ApiRef_1f318282-a1f9-40a7-8272-448727603f04.xml, fltuser/FilterCreate, ifsk.filtercreate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fltuser.h
req.include-header: Fltuser.h
req.target-type: Universal
req.target-min-winverclnt: 
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
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FilterCreate function


## -description


The <b>FilterCreate</b> function creates a handle for the given minifilter. 


## -parameters




### -param lpFilterName [in]

Pointer to a null-terminated wide-character string containing the name of the minifilter. This parameter is required and cannot be <b>NULL</b>. 


### -param hFilter [out]

Pointer to a caller-allocated variable that receives a handle for the minifilter if the call to <b>FilterCreate</b> succeeds; otherwise, it receives INVALID_HANDLE_VALUE. 


## -returns



<b>FilterCreate</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



A user-mode application calls <b>FilterCreate</b> to create a handle that can be used to communicate with a kernel-mode minifilter. The returned minifilter handle can be passed as a parameter to functions such as <a href="https://msdn.microsoft.com/d5124ac2-dd1e-46b2-b25c-e965768eaf9e">FilterGetInformation</a>. 

To close a filter handle returned by <b>FilterCreate</b>, call <a href="https://msdn.microsoft.com/c5d3774e-6f57-4a6b-97a8-623268884859">FilterClose</a>. 




## -see-also




<a href="https://msdn.microsoft.com/c5d3774e-6f57-4a6b-97a8-623268884859">FilterClose</a>



<a href="https://msdn.microsoft.com/d5124ac2-dd1e-46b2-b25c-e965768eaf9e">FilterGetInformation</a>
 

 

