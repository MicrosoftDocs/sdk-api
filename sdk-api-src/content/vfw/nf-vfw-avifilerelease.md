---
UID: NF:vfw.AVIFileRelease
title: AVIFileRelease function
author: windows-sdk-content
description: The AVIFileRelease function decrements the reference count of an AVI file interface handle and closes the file if the count reaches zero.
old-location: multimedia\avifilerelease.htm
tech.root: Multimedia
ms.assetid: c2f94ca2-b46c-48b0-9c31-92cf2cf75be3
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: AVIFileRelease, AVIFileRelease function [Windows Multimedia], _win32_AVIFileRelease, multimedia.avifilerelease, vfw/AVIFileRelease
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
 - AVIFileRelease
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIFileRelease function


## -description



The <b>AVIFileRelease</b> function decrements the reference count of an AVI file interface handle and closes the file if the count reaches zero.



This function supersedes the obsolete <b>AVIFileClose</b> function.


## -parameters




### -param pfile

Handle to an open AVI file.


## -returns



Returns the reference count of the file. This return value should be used only for debugging purposes.




## -remarks



The argument <i>pfile</i> is a pointer to an <a href="https://msdn.microsoft.com/401db941-cbf6-452b-84e2-605fafac8a6d">IAVIFile</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

