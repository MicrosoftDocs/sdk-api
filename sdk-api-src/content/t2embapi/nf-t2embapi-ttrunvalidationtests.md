---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# TTRunValidationTests function


## -description


Validates part or all glyph data of a wide-character (16-bit) font, in the size range specified.

<b>Windows Vista and later</b>: this function will always return E_API_NOTIMPL, and no processing is performed by this API.


## -parameters




### -param hDC [in]

Device context handle.


### -param pTestParam [in]

Pointer to a <a href="https://msdn.microsoft.com/901fd8e5-1602-4e20-9269-d0c3fe661e45">TTVALIDATIONTESTPARAMS</a> structure specifying the parameters to test.


## -returns



If successful and the glyph data is valid, returns E_NONE.

Otherwise, returns an error code described in <a href="https://msdn.microsoft.com/71effafe-55a9-40ed-81c7-07278eba32d3">Embedding-Function Error Messages</a>.




## -remarks



This function was supported in Windows XP and earlier, but is no longer supported. In Windows Vista and later, this function will always return E_API_NOTIMPL, and no processing is performed by this API.

Effective font validation can be performed by a tool, such as Font Validator, that is capable of performing thorough validation of all parts of the font file. See the <a href="http://www.microsoft.com/typography/FontValidator.mspx">Font Validator documentation</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/4b4fdd3f-c07c-407c-87eb-5bd8a1620d75">TTRunValidationTestsEx</a>



<a href="https://msdn.microsoft.com/901fd8e5-1602-4e20-9269-d0c3fe661e45">TTVALIDATIONTESTPARAMS</a>
 

 

