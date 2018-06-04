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

# DWRITE_TRIMMING structure


## -description


Specifies the trimming option for text overflowing the layout box. 


## -struct-fields




### -field granularity

Type: <b><a href="https://msdn.microsoft.com/81ab22cd-7b7f-4db6-9f67-2cafd54f4621">DWRITE_TRIMMING_GRANULARITY</a></b>

A value that specifies  the text granularity used to trim text overflowing the layout box.


### -field delimiter

Type: <b>UINT32</b>

A character code used as the delimiter that signals the beginning of the portion of text to be preserved. 
          Text starting from the Nth occurence of the delimiter (where N equals delimiterCount) counting backwards from the end of the text block will be preserved.
          For example, given the text is a path like c:\A\B\C\D\file.txt and delimiter equal to '\' and delimiterCount equal to 1, the file.txt portion of the text would be preserved.  
          Specifying a delimiterCount of 2 would preserve D\file.txt.
          


### -field delimiterCount

Type: <b>UINT32</b>

The delimiter count, counting from the end of the text, to preserve text from.

