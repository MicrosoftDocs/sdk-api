---
UID: NF:fci.FCIDestroy
title: FCIDestroy function
author: windows-sdk-content
description: The FCIDestroy function deletes an open FCI context, freeing any memory and temporary files associated with the context.
old-location: winprog\fcidestroy.htm
tech.root: devnotes
ms.assetid: bb1a6294-664f-450f-b8ec-d6f8957d920e
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: FCIDestroy, FCIDestroy function [Windows API], fci/FCIDestroy, winprog.fcidestroy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fci.h
req.include-header: 
req.target-type: Windows
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
req.lib: Cabinet.lib
req.dll: Cabinet.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cabinet.dll
api_name:
 - FCIDestroy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FCIDestroy function


## -description


The <b>FCIDestroy</b> function deletes an open  FCI context, freeing any memory and temporary files associated with the context.


## -parameters




### -param hfci [in]

A valid FCI context handle returned by the <a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a> function.


## -returns



If the function succeeds, it returns <b>TRUE</b>; otherwise, <b>FALSE</b>.

Extended error information is provided in the <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure used to create the FCI context.




## -see-also




<a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a>
 

 

