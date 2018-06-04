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

# WS_CHARSET enumeration


## -description


Identifies the character set of a document.


## -enum-fields




### -field WS_CHARSET_AUTO


          Specifies that the charset of a document should be determined automatically by inspecting
          the BOM (Byte Order Marks) of the document and the xml declaration if present.
        


### -field WS_CHARSET_UTF8


          Specifies that the charset of a document is UTF-8.
        


### -field WS_CHARSET_UTF16LE


          Specifies that the charset of a document is UTF-16LE.
        


### -field WS_CHARSET_UTF16BE


          Specifies that the charset of a document is UTF-16BE.
        

