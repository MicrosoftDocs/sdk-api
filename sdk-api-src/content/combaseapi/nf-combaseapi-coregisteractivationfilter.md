---
UID: NF:combaseapi.CoRegisterActivationFilter
title: CoRegisterActivationFilter function
author: windows-sdk-content
description: Registers a process-wide filter to process activation requests.
old-location: com\coregisteractivationfilter.htm
old-project: com
ms.assetid: 4189633F-9B14-4EAD-84BD-F74355376164
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CoRegisterActivationFilter, CoRegisterActivationFilter function [COM], com.coregisteractivationfilter, combaseapi/CoRegisterActivationFilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.redist: 
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
tech.root: 
req.typenames: REGCLS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - ComBase.dll
api_name:
 - CoRegisterActivationFilter
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# CoRegisterActivationFilter function


## -description


Registers a process-wide filter to process activation requests.


## -parameters




### -param pActivationFilter [in]

Pointer to the filter to register.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This registers one and only one process-wide filter.



