---
UID: NF:fdi.FDIDestroy
title: FDIDestroy function
author: windows-sdk-content
description: The FDIDestroy function deletes an open FDI context.
old-location: winprog\fdidestroy.htm
old-project: devnotes
ms.assetid: fe3b8045-a476-4a21-b732-0d4799798faf
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FDIDestroy, FDIDestroy function [Windows API], fdi/FDIDestroy, winprog.fdidestroy
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
 - FDIDestroy
product: Windows
targetos: Windows
req.lib: Cabinet.lib
req.dll: Cabinet.dll
req.irql: 
req.product: Internet Explorer 5
---

# FDIDestroy function


## -description


The <b>FDIDestroy</b> function deletes an open FDI context.


## -parameters




### -param hfdi [in]

 A valid FDI context handle returned by  the <a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a> function.


## -returns



If the function succeeds, it returns <b>TRUE</b>; otherwise, <b>FALSE</b>.

Extended error information is provided in the <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure used to create the FDI context.




## -see-also




<a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a>
 

 

