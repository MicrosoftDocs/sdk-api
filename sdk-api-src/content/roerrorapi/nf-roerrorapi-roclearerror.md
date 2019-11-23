---
UID: NF:roerrorapi.RoClearError
title: RoClearError function

description: Removes existing error information from the current thread environment block (TEB).
old-location: winrt\roclearerror.htm
tech.root: WinRT
ms.assetid: 082B26B2-3B17-45E3-8D4B-0E27777EDFF6

ms.date: 12/5/2018
ms.keywords: RoClearError, RoClearError function [Windows Runtime], roerrorapi/RoClearError, winrt.roclearerror
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
f1_keywords: 
 - "roerrorapi/RoClearError"
dev_langs:
 - c++
req.header: roerrorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-WinRT-error-l1-1-1.dll
api_name:
 - RoClearError
targetos: Windows
req.typenames: 
req.redist: 
---

# RoClearError function


## -description


Removes existing error information from the current thread environment block (TEB).


## -parameters






## -returns



This function does not return a value.




## -remarks



Call the <b>RoClearError</b> function to remove existing thread error information from the thread environment block (TEB). If COM is not initialized, this call does nothing to create the TEB slot for this information. Language projections call this function to ensure there's no stale error information on the thread.



