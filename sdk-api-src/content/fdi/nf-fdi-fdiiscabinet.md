---
UID: NF:fdi.FDIIsCabinet
title: FDIIsCabinet function
author: windows-sdk-content
description: The FDIIsCabinet function determines whether a file is a cabinet and, if it is, returns information about it.
old-location: winprog\fdiiscabinet.htm
old-project: devnotes
ms.assetid: 01d223ca-56c6-49fa-b9e6-e5eeda88936a
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FDIIsCabinet, FDIIsCabinet function [Windows API], fdi/FDIIsCabinet, winprog.fdiiscabinet
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: CCAB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cabinet.dll
api_name:
 - FDIIsCabinet
product: Windows
targetos: Windows
req.lib: Cabinet.lib
req.dll: Cabinet.dll
req.irql: 
req.product: Internet Explorer 5
---

# FDIIsCabinet function


## -description


The <b>FDIIsCabinet</b> function determines whether a file is a cabinet and, if it is, returns information about it.


## -parameters




### -param hfdi [in]

A valid FDI context handle returned  by <a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a>.


### -param hf [in]

An application-defined value to keep track of the opened file. This value must be of the same type as values used by the File I/O functions passed to <a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a>.


### -param pfdici [in, out]

Pointer to an <a href="https://msdn.microsoft.com/fde1a2ca-60cd-4a4d-9872-681e2f8f4fb1">FDICABINETINFO</a> structure that receives the cabinet details, in the event the file is actually a cabinet.


## -returns



If the file is a cabinet, the function returns <b>TRUE</b> ; otherwise, <b>FALSE</b>.

Extended error information is provided in the <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure used to create the FDI context.




## -see-also




<a href="https://msdn.microsoft.com/fde1a2ca-60cd-4a4d-9872-681e2f8f4fb1">FDICABINETINFO</a>



<a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a>



<a href="https://msdn.microsoft.com/c923b0a5-1a8d-42aa-bd05-0d318199756d">FDITruncateCabinet</a>
 

 

