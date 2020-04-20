---
UID: NF:vfw.capGetDriverDescriptionA
title: capGetDriverDescriptionA function (vfw.h)
description: The capGetDriverDescription function retrieves the version description of the capture driver.helpviewer_keywords: ["_win32_capGetDriverDescription","capGetDriverDescription","capGetDriverDescription function [Windows Multimedia]","capGetDriverDescriptionA","capGetDriverDescriptionW","multimedia.capgetdriverdescription","vfw/capGetDriverDescription","vfw/capGetDriverDescriptionA","vfw/capGetDriverDescriptionW"]
old-location: multimedia\capgetdriverdescription.htm
tech.root: Multimedia
ms.assetid: 97ec77f8-79fe-4c0b-9b73-5b09903c47b2
ms.date: 12/05/2018
ms.keywords: _win32_capGetDriverDescription, capGetDriverDescription, capGetDriverDescription function [Windows Multimedia], capGetDriverDescriptionA, capGetDriverDescriptionW, multimedia.capgetdriverdescription, vfw/capGetDriverDescription, vfw/capGetDriverDescriptionA, vfw/capGetDriverDescriptionW
f1_keywords:
- vfw/capGetDriverDescription
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-functions">Video Capture Functions</a>
 

 

