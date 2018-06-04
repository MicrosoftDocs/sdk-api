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

# ImmEnumRegisterWordW function


## -description


Enumerates the register strings having the specified reading string, style, and register string.


## -parameters




### -param HKL

TBD


### -param REGISTERWORDENUMPROCW

TBD


### -param lpszReading [in, optional]

Pointer to the reading string to enumerate. The application sets this parameter to <b>NULL</b> if the function is to enumerate all available reading strings that match the <i>dwStyle</i> and <i>lpszRegister</i> settings.


### -param DWORD

TBD


### -param lpszRegister [in, optional]

Pointer to the register string to enumerate. The application sets this parameter to <b>NULL</b> if the function is to enumerate all register strings that match the <i>lpszReading</i> and <i>dwStyle</i> settings.


### -param LPVOID

TBD




#### - dwStyle [in]

Style to enumerate. The application specifies 0 if the function is to enumerate all available styles that match the <i>lpszReading</i> and <i>lpszRegister</i> settings.


#### - hKL [in]

Input locale identifier.


#### - lpData [in]

Pointer to application-supplied data. The function passes this data to the callback function.


#### - lpfnEnumProc [in]

Pointer to the callback function. For more information, see <a href="https://msdn.microsoft.com/06038c87-3553-47de-ba9f-b9c65ea9920b">EnumRegisterWordProc</a>.


## -returns



Returns the last value returned by the callback function, with the meaning defined by the application. The function returns 0 if it cannot enumerate the register strings.




## -remarks



If <i>dwStyle</i> is set to 0 and both <i>lpszReading</i> and <i>lpszRegister</i> are set to <b>NULL</b>, this function enumerates all register strings in the IME dictionary.




## -see-also




<a href="https://msdn.microsoft.com/06038c87-3553-47de-ba9f-b9c65ea9920b">EnumRegisterWordProc</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

