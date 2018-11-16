---
UID: NF:vfw.AVIFileAddRef
title: AVIFileAddRef function
author: windows-sdk-content
description: The AVIFileAddRef function increments the reference count of an AVI file.
old-location: multimedia\avifileaddref.htm
tech.root: Multimedia
ms.assetid: f3dd4fa0-69e3-4249-8c74-7502d09ff341
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AVIFileAddRef, AVIFileAddRef function [Windows Multimedia], _win32_AVIFileAddRef, multimedia.avifileaddref, vfw/AVIFileAddRef
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
api_name:
 - AVIFileAddRef
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- AVIFileAddRef
: 
---

# AVIFileAddRef function


## -description



The <b>AVIFileAddRef</b> function increments the reference count of an AVI file.




## -parameters




### -param pfile

Handle to an open AVI file.


## -returns



Returns the updated reference count for the file interface.




## -remarks



The argument <i>pfile</i> is a pointer to an <a href="https://msdn.microsoft.com/401db941-cbf6-452b-84e2-605fafac8a6d">IAVIFile</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

