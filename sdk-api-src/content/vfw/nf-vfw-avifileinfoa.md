---
UID: NF:vfw.AVIFileInfoA
title: AVIFileInfoA function
author: windows-sdk-content
description: The AVIFileInfo function obtains information about an AVI file.
old-location: multimedia\avifileinfo.htm
tech.root: Multimedia
ms.assetid: 10d7decf-a133-4d55-93d5-867952307819
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: AVIFileInfo, AVIFileInfo function [Windows Multimedia], AVIFileInfoA, AVIFileInfoW, _win32_AVIFileInfo, multimedia.avifileinfo, vfw/AVIFileInfo, vfw/AVIFileInfoA, vfw/AVIFileInfoW
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
req.unicode-ansi: AVIFileInfoW (Unicode) and AVIFileInfoA (ANSI)
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
 - AVIFileInfo
 - AVIFileInfoA
 - AVIFileInfoW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIFileInfoA function


## -description



The <b>AVIFileInfo</b> function obtains information about an AVI file.




## -parameters




### -param pfile

Handle to an open AVI file.


### -param pfi

Pointer to the structure used to return file information. Typically, this parameter points to an <a href="https://msdn.microsoft.com/d3fda342-2ade-41b1-b709-c194f132e015">AVIFILEINFO</a> structure.


### -param lSize

Size, in bytes, of the structure.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



The argument <i>pfile</i> is a pointer to an <a href="https://msdn.microsoft.com/401db941-cbf6-452b-84e2-605fafac8a6d">IAVIFile</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

