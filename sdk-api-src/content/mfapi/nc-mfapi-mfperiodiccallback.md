---
UID: NC:mfapi.MFPERIODICCALLBACK
title: MFPERIODICCALLBACK
author: windows-driver-content
description: Callback function for the MFAddPeriodicCallback function.
old-location: mf\mfperiodiccallback_callback.htm
old-project: medfound
ms.assetid: 9449fa04-867c-4f27-a05c-ff0d6e912c53
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: 9449fa04-867c-4f27-a05c-ff0d6e912c53, MFPERIODICCALLBACK, MFPERIODICCALLBACK function pointer [Media Foundation], mf.mfperiodiccallback_callback, mfapi/MFPERIODICCALLBACK
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WIN32_MEMORY_REGION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	mfapi.h
api_name:
-	MFPERIODICCALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MFPERIODICCALLBACK callback


## -description



Callback function for the <a href="https://msdn.microsoft.com/e5898fc8-72e9-45cc-8e85-4410ed7cc512">MFAddPeriodicCallback</a> function.




## -parameters




### -param *pContext [in]

Pointer to the <b>IUnknown</b> interface, or <b>NULL</b>. This pointer is specified by the caller in the <a href="https://msdn.microsoft.com/e5898fc8-72e9-45cc-8e85-4410ed7cc512">MFAddPeriodicCallback</a> function.


## -returns



This function pointer does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

