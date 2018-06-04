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

# IItemNameLimits::GetValidCharacters


## -description


Loads a string that contains each of the characters that are valid or invalid in the namespace under which it is called.


## -parameters




### -param ppwszValidChars [out]

Type: <b>LPWSTR*</b>

A pointer to a string that contains all valid characters in the namespace. If the namespace provides <i>any</i> invalid characters in <i>ppwszInvalidChars</i>, then this value returns <b>NULL</b>. See Remarks for more details.


### -param ppwszInvalidChars [out]

Type: <b>LPWSTR*</b>

A pointer to a string that contains all invalid characters in the namespace.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



As an example, the standard file system returns the string "\/:*?"&lt;&gt;|" in <i>ppwszInvalidChars</i> and <b>NULL</b> in <i>ppwszValidChars</i>. 

Both parameters cannot return non-<b>NULL</b> values, so <i>ppwszValidChars</i> is assigned a value of <b>NULL</b> because of the non-<b>NULL</b> value 

in <i>ppwszInvalidChars</i>. It is assumed that when there are specified invalid characters, everything else is valid. Only when <i>ppwszInvalidChars</i> is <b>NULL</b> does <i>ppwszValidChars</i> contain a list of all valid characters.
			

If the method returns a success code, the allocated string must be freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


			



