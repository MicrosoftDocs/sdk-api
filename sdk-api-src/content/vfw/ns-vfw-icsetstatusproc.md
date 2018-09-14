---
UID: NS:vfw.ICSETSTATUSPROC
title: ICSETSTATUSPROC
author: windows-sdk-content
description: The ICSETSTATUSPROC structure contains status information used with the ICM_SET_STATUS_PROC message.
old-location: multimedia\icsetstatusproc_struct.htm
tech.root: Multimedia
ms.assetid: 32f115a4-3096-4af0-a254-1bac39a830d7
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ICSETSTATUSPROC, ICSETSTATUSPROC structure [Windows Multimedia], multimedia.icsetstatusproc_COLLISION563, multimedia.icsetstatusproc_struct, vfw/ICSETSTATUSPROC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICSETSTATUSPROC
product: Windows
targetos: Windows
req.typenames: ICSETSTATUSPROC
req.redist: 
---

# ICSETSTATUSPROC structure


## -description



The <b>ICSETSTATUSPROC</b> structure contains status information used with the <a href="https://msdn.microsoft.com/a1bcd840-b94b-487e-91d6-67411a8a3a2d">ICM_SET_STATUS_PROC</a> message.




## -struct-fields




### -field dwFlags

Reserved; set to zero.


### -field lParam

Parameter that contains a constant to pass to the status procedure.


### -field Status

 




#### - fpfnStatus

Pointer to the status function. Specify <b>NULL</b> if status messages should not be sent. For more information about the callback function, see the <a href="https://msdn.microsoft.com/a24b8a05-71f3-488b-a521-5c43955c5ed2">MyStatusProc</a> function.


## -see-also




<a href="https://msdn.microsoft.com/a1bcd840-b94b-487e-91d6-67411a8a3a2d">ICM_SET_STATUS_PROC</a>



<a href="https://msdn.microsoft.com/a24b8a05-71f3-488b-a521-5c43955c5ed2">MyStatusProc</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>



<a href="https://msdn.microsoft.com/129a65a7-cac3-47e0-9e9c-6e5a4a260c73">Video Compression Structures</a>
 

 

