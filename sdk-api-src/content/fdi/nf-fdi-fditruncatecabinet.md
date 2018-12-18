---
UID: NF:fdi.FDITruncateCabinet
title: FDITruncateCabinet function
author: windows-sdk-content
description: The FDITruncateCabinet function truncates a cabinet file starting at the specified folder number.
old-location: winprog\fditruncatecabinet.htm
tech.root: devnotes
ms.assetid: c923b0a5-1a8d-42aa-bd05-0d318199756d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FDITruncateCabinet, FDITruncateCabinet function [Windows API], fdi/FDITruncateCabinet, winprog.fditruncatecabinet
ms.topic: function
req.header: fdi.h
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
 - FDITruncateCabinet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FDITruncateCabinet function


## -description


The <b>FDITruncateCabinet</b> function truncates a cabinet file starting at the specified folder number.


## -parameters




### -param hfdi [in]

A valid FDI context handle returned by the <a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a> function.


### -param pszCabinetName [in]

The full cabinet filename.


### -param iFolderToDelete [in]

The index of the first folder to delete.


## -returns



If the function succeeds, it returns <b>TRUE</b>; otherwise, <b>FALSE</b>.

Extended error information is provided in the <a href="https://msdn.microsoft.com/en-us/library/Bb432257(v=VS.85).aspx">ERF</a> structure used to create the FDI context.




## -see-also




<a href="https://msdn.microsoft.com/01d223ca-56c6-49fa-b9e6-e5eeda88936a">FDIIsCabinet</a>
 

 

