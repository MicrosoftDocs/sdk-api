---
UID: NF:vfw.EditStreamSetNameW
title: EditStreamSetNameW function
author: windows-sdk-content
description: The EditStreamSetName function assigns a descriptive string to a stream.
old-location: multimedia\editstreamsetname.htm
tech.root: Multimedia
ms.assetid: 33542ad1-4bee-4051-8b75-f5328086250b
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: EditStreamSetName, EditStreamSetName function [Windows Multimedia], EditStreamSetNameA, EditStreamSetNameW, _win32_EditStreamSetName, multimedia.editstreamsetname, vfw/EditStreamSetName, vfw/EditStreamSetNameA, vfw/EditStreamSetNameW
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
req.unicode-ansi: EditStreamSetNameW (Unicode) and EditStreamSetNameA (ANSI)
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
 - EditStreamSetName
 - EditStreamSetNameA
 - EditStreamSetNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EditStreamSetNameW function


## -description



The <b>EditStreamSetName</b> function assigns a descriptive string to a stream.




## -parameters




### -param pavi

Handle to an open stream.


### -param lpszName

Null-terminated string containing the description of the stream.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



This function updates the <b>szName</b> member of the <b>AVISTREAMINFO</b> structure.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

