---
UID: NC:mfapi.MFPERIODICCALLBACK
title: MFPERIODICCALLBACK
author: windows-sdk-content
description: Callback function for the MFAddPeriodicCallback function.
old-location: mf\mfperiodiccallback_callback.htm
tech.root: medfound
ms.assetid: 9449fa04-867c-4f27-a05c-ff0d6e912c53
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 9449fa04-867c-4f27-a05c-ff0d6e912c53, MFPERIODICCALLBACK, MFPERIODICCALLBACK callback, MFPERIODICCALLBACK callback function [Media Foundation], mf.mfperiodiccallback_callback, mfapi/MFPERIODICCALLBACK
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - mfapi.h
api_name:
 - MFPERIODICCALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFPERIODICCALLBACK callback function


## -description



Callback function for the <a href="https://msdn.microsoft.com/e5898fc8-72e9-45cc-8e85-4410ed7cc512">MFAddPeriodicCallback</a> function.




## -parameters




### -param *pContext [in]

Pointer to the <b>IUnknown</b> interface, or <b>NULL</b>. This pointer is specified by the caller in the <a href="https://msdn.microsoft.com/e5898fc8-72e9-45cc-8e85-4410ed7cc512">MFAddPeriodicCallback</a> function.


## -returns



This callback function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

