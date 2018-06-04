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

# TTRunValidationTestsEx function


## -description


Validates part or all glyph data of a UCS-4 character (32-bit) font, in the size range specified.

<b>Windows Vista and later</b>: this function will always return E_API_NOTIMPL, and no processing is performed by this API.


## -parameters




### -param hDC [in]

Device context handle.


### -param pTestParam [in]

Pointer to a <a href="https://msdn.microsoft.com/03bcfb1a-6ed8-4e78-b3c8-64d29dc74dbc">TTVALIDATIONTESTPARAMSEX</a> structure specifying the parameters to test.


## -returns



If successful and the glyph data is valid, returns E_NONE.

Otherwise, returns an error code described in <a href="https://msdn.microsoft.com/71effafe-55a9-40ed-81c7-07278eba32d3">Embedding-Function Error Messages</a>.




## -remarks



<b>TTRunValidationTestsEx</b> is a UCS-4 version of <a href="https://msdn.microsoft.com/fe60938b-c728-49a9-89b4-495b2364091a">TTRunValidationTests</a>.

This function was supported in Windows XP and earlier, but is no longer supported. In Windows Vista and later, this function will always return E_API_NOTIMPL, and no processing is performed by this API.

Effective font validation can be performed by a tool, such as Font Validator, that is capable of performing thorough validation of all parts of the font file. Please see <a href="http://www.microsoft.com/typography/FontValidator.mspx">http://www.microsoft.com/typography/FontValidator.mspx</a> for information on the Font Validator tool.




## -see-also




<a href="https://msdn.microsoft.com/fe60938b-c728-49a9-89b4-495b2364091a">TTRunValidationTests</a>



<a href="https://msdn.microsoft.com/03bcfb1a-6ed8-4e78-b3c8-64d29dc74dbc">TTVALIDATIONTESTPARAMSEX</a>
 

 

