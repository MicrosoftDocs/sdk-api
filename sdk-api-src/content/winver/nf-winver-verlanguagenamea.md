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

# VerLanguageNameA function


## -description


Retrieves a description string for the language associated with a specified binary Microsoft language identifier.


## -parameters




### -param wLang [in]

Type: <b>DWORD</b>

The binary language identifier. For a complete list of the language identifiers, see <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">Language Identifiers</a>.

For example, the description string associated with the language identifier 0x040A is "Spanish (Traditional Sort)". If the identifier is unknown, the <i>szLang</i> parameter points to a default string ("Language Neutral").


### -param szLang [out]

Type: <b>LPTSTR</b>

The language specified by the <i>wLang</i> parameter. 


### -param cchLang [in]

Type: <b>DWORD</b>

The size, in characters, of the buffer pointed to by <i>szLang</i>.


## -returns



Type: <b>DWORD</b>

The return value is the size, in characters, of the string returned in the buffer. This value does not include the terminating null character. If the description string is smaller than or equal to the buffer, the entire description string is in the buffer. If the description string is larger than the buffer, the description string is truncated to the length of the buffer.

If an error occurs, the return value is zero. Unknown language identifiers do not produce errors. 




## -remarks



 This function works on 16-, 32-, and 64-bit file images.

Typically, an installation program uses this function to translate a language identifier returned by the <a href="https://msdn.microsoft.com/4fc3e2f0-0d9b-4974-b091-98908691bb14">VerQueryValue</a> function. The text string may be used in a dialog box that asks the user how to proceed in the event of a language conflict. 




## -see-also




<a href="https://msdn.microsoft.com/60de7900-56b9-4481-bef9-b4079eedf926">Version Information Overview</a>
 

 

