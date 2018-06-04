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

# TTGetNewFontName function


## -description


Obtains the family name for the font loaded through <a href="https://msdn.microsoft.com/85181d86-bc18-4948-bc7d-65c2d71efefb">TTLoadEmbeddedFont</a>.


## -parameters




### -param phFontReference [in]

Handle that identifies the embedded font that has been installed. The handle references an internal structure, not an Hfont.


### -param wzWinFamilyName

TBD


### -param cchMaxWinName [in]

Length of the string allocated for the Windows name (<i>szWinFamilyName</i>). Must be at least LF_FACESIZE long.


### -param szMacFamilyName [out]

Buffer to hold the new 8-bit-character MacIntosh family name.


### -param cchMaxMacName [in]

Length of the string allocated for the Macintosh name (<i>szMacFamilyName</i>). Must be at least LF_FACESIZE long.


#### - szWinFamilyName [out]

Buffer to hold the new 16-bit-character Microsoft Windows family name.


## -returns



If successful, returns E_NONE.

The font family name is a string in <i>szWinFamilyName</i> or <i>szMacFamilyName</i>.

Otherwise, returns an error code described in <a href="https://msdn.microsoft.com/71effafe-55a9-40ed-81c7-07278eba32d3">Embedding-Function Error Messages</a>.




## -remarks



<div class="alert"><b>Note</b>  This function returns the font family name in the appropriate string buffer, either for Windows or the MacIntosh. The buffer for the other operating system is not used.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0ce9ade0-df5b-4a2a-adf6-ca641e27d2bd">TTGetEmbeddedFontInfo</a>



<a href="https://msdn.microsoft.com/c442447f-221d-4bce-9749-fb9fbe333808">TTGetEmbeddingType</a>



<a href="https://msdn.microsoft.com/85181d86-bc18-4948-bc7d-65c2d71efefb">TTLoadEmbeddedFont</a>
 

 

