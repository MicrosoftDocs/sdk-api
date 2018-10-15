---
UID: NF:vfw.AVIFileInit
title: AVIFileInit function
author: windows-sdk-content
description: The AVIFileInit function initializes the AVIFile library.
old-location: multimedia\avifileinit.htm
tech.root: Multimedia
ms.assetid: 3246a7d2-4b17-413d-b0d5-82146c993f26
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: AVIFileInit, AVIFileInit function [Windows Multimedia], _win32_AVIFileInit, multimedia.avifileinit, vfw/AVIFileInit
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
 - Ext-MS-Win-Media-Avi-L1-1-0.dll
api_name:
 - AVIFileInit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIFileInit function


## -description



The <b>AVIFileInit</b> function initializes the AVIFile library.



The AVIFile library maintains a count of the number of times it is initialized, but not the number of times it was released. Use the <a href="https://msdn.microsoft.com/2daa509a-9e95-4f49-8195-97d3e7cd17b4">AVIFileExit</a> function to release the AVIFile library and decrement the reference count. Call <b>AVIFileInit</b> before using any other AVIFile functions.

This function supersedes the obsolete <b>AVIStreamInit</b> function.


## -parameters






## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

