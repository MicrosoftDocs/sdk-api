---
UID: NF:vfw.capGetDriverDescriptionA
title: capGetDriverDescriptionA function
author: windows-sdk-content
description: The capGetDriverDescription function retrieves the version description of the capture driver.
old-location: multimedia\capgetdriverdescription.htm
tech.root: Multimedia
ms.assetid: 97ec77f8-79fe-4c0b-9b73-5b09903c47b2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_win32_capGetDriverDescription, capGetDriverDescription, capGetDriverDescription function [Windows Multimedia], capGetDriverDescriptionA, capGetDriverDescriptionW, multimedia.capgetdriverdescription, vfw/capGetDriverDescription, vfw/capGetDriverDescriptionA, vfw/capGetDriverDescriptionW"
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
req.unicode-ansi: capGetDriverDescriptionW (Unicode) and capGetDriverDescriptionA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: Avicap32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avicap32.dll
api_name:
 - capGetDriverDescription
 - capGetDriverDescriptionA
 - capGetDriverDescriptionW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- capGetDriverDescriptionA
: 
---

# capGetDriverDescriptionA function


## -description



The <b>capGetDriverDescription</b> function retrieves the version description of the capture driver.




## -parameters




### -param wDriverIndex

Index of the capture driver. The index can range from 0 through 9.

Plug-and-Play capture drivers are enumerated first, followed by capture drivers listed in the registry, which are then followed by capture drivers listed in SYSTEM.INI.


### -param lpszName

Pointer to a buffer containing a null-terminated string corresponding to the capture driver name.


### -param cbName

Length, in bytes, of the buffer pointed to by <i>lpszName</i>.


### -param lpszVer

Pointer to a buffer containing a null-terminated string corresponding to the description of the capture driver.


### -param cbVer

Length, in bytes, of the buffer pointed to by <i>lpszVer</i>.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.




## -remarks



If the information description is longer than its buffer, the description is truncated. The returned string is always null-terminated. If a buffer size is zero, its corresponding description is not copied.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/0fe87fa7-9f07-48f7-958b-da385d9ddaf0">Video Capture Functions</a>
 

 

