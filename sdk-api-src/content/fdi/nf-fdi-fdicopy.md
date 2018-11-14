---
UID: NF:fdi.FDICopy
title: FDICopy function
author: windows-sdk-content
description: The FDICopy function extracts files from cabinets.
old-location: winprog\fdicopy.htm
tech.root: devnotes
ms.assetid: 6ec2b10b-f70a-4a22-beff-df6b6a4c4cfd
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: FDICopy, FDICopy function [Windows API], fdi/FDICopy, winprog.fdicopy
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - FDICopy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- FDICopy
: 
---

# FDICopy function


## -description


The <b>FDICopy</b> function extracts files from cabinets.


## -parameters




### -param hfdi [in]

A valid FDI context handle returned by the <a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a> function.


### -param pszCabinet [in]

The name of the cabinet file, excluding any path information, from which to extract files. If a file is split over multiple cabinets, <b>FDICopy</b>  allows for subsequent cabinets to be opened.


### -param pszCabPath [in]

The pathname of the cabinet file, but not including the name of the file itself. For example, "C:\MyCabs\". 

The contents of <i>pszCabinet</i> are appended to <i>pszCabPath</i> to create the full pathname of the cabinet.


### -param flags [in]

No flags are currently defined and this parameter should be set to zero.


### -param pfnfdin [in]

Pointer to an application-defined callback notification function to update the application on the status of the decoder. The function should be declared using the <a href="https://msdn.microsoft.com/7655ddb2-7cd4-4012-913c-9909fcea639a">FNFDINOTIFY</a> macro.


### -param pfnfdid [in]

Not currently used by FDI. This parameter should be set to <b>NULL</b>.


### -param pvUser [in, optional]

Pointer to an application-specified value to pass to the notification function.


## -returns



If the function succeeds, it returns <b>TRUE</b>; otherwise, <b>FALSE</b>.

Extended error information is provided in the <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure used to create the FDI context.




## -see-also




<a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a>
 

 

