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

# GetCurrentThemeName function


## -description


Retrieves the name of the current visual style, and optionally retrieves the color scheme name and size name.


## -parameters




### -param pszThemeFileName [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a></b>

Pointer to a string that receives the theme path and file name.


### -param cchMaxNameChars

TBD


### -param pszColorBuff [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a></b>

Pointer to a string that receives the color scheme name. This parameter may be set to <b>NULL</b>.


### -param cchMaxColorChars [in]

Type: <b>int</b>

Value of type <b>int</b> that contains the maximum number of characters allowed in the color scheme name.


### -param pszSizeBuff [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a></b>

Pointer to a string that receives the size name. This parameter may be set to <b>NULL</b>.


### -param cchMaxSizeChars [in]

Type: <b>int</b>

Value of type <b>int</b> that contains the maximum number of characters allowed in the size name.


#### - dwMaxNameChars [in]

Type: <b>int</b>

Value of type <b>int</b> that contains the maximum number of characters allowed in the theme file name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful, otherwise an error code.



