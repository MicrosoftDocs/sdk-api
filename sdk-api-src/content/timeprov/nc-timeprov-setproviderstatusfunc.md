---
UID: NC:timeprov.SetProviderStatusFunc
title: SetProviderStatusFunc (timeprov.h)
description: Sets the time provider's status information.
old-location: base\setproviderstatusfunc.htm
tech.root: SysInfo
ms.assetid: e52dd1d3-081a-4fcc-85d9-a1dcef0e8011
ms.date: 12/05/2018
ms.keywords: SetProviderStatusFunc, SetProviderStatusFunc callback, SetProviderStatusFunc callback function, _win32_setproviderstatusfunc, base.setproviderstatusfunc, timeprov/SetProviderStatusFunc
f1_keywords:
- timeprov/SetProviderStatusFunc
dev_langs:
- c++
req.header: timeprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Timeprov.h
api_name:
- SetProviderStatusFunc
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetProviderStatusFunc callback function


## -description


Sets the time provider's status information.


## -parameters




### -param *pspsi [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/timeprov/ns-timeprov-setproviderstatusinfo">SetProviderStatusInfo</a> structure that provides the status information.


## -returns



If the function succeeds, the return value is S_OK. Otherwise, the return value is one of the error codes defined in WinError.h.




## -remarks



The 
<a href="https://docs.microsoft.com/windows/desktop/api/timeprov/nf-timeprov-timeprovopen">TimeProvOpen</a> function returns a pointer to this function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/timeprov/ns-timeprov-setproviderstatusinfo">SetProviderStatusInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/timeprov/nf-timeprov-timeprovopen">TimeProvOpen</a>
 

 

