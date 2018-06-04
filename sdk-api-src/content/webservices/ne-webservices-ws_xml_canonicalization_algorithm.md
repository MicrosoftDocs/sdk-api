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

# WS_XML_CANONICALIZATION_ALGORITHM enumeration


## -description


The values for the XML canonicalization algorithms.
      


## -enum-fields




### -field WS_EXCLUSIVE_XML_CANONICALIZATION_ALGORITHM


          The exclusive XML canonicalization algorithm
          represented by the URI 'http://www.w3.org/2001/10/xml-exc-c14n#' and
          defined in <a href=" http://go.microsoft.com/fwlink/p/?linkid=139714">RFC 3741</a>.
        


### -field WS_EXCLUSIVE_WITH_COMMENTS_XML_CANONICALIZATION_ALGORITHM


          The exclusive XML canonicalization with comments algorithm
          defined in <a href=" http://go.microsoft.com/fwlink/p/?linkid=139714">RFC 3741</a>.
        


### -field WS_INCLUSIVE_XML_CANONICALIZATION_ALGORITHM


          The inclusive XML canonicalization algorithm
          defined in <a href="http://go.microsoft.com/fwlink/p/?linkid=139716">Canonical XML
Version 1.0</a>.
        


          Inclusive canonicalization can only be applied to entire xml documents.
        


### -field WS_INCLUSIVE_WITH_COMMENTS_XML_CANONICALIZATION_ALGORITHM


          The inclusive XML canonicalization with comments algorithm
          represented by the URI 'http://www.w3.org/TR/2001/REC-xml-c14n-20010315#WithComments' and
          defined in <a href="http://go.microsoft.com/fwlink/p/?linkid=139716">Canonical XML
Version 1.0</a>.
        


          Inclusive canonicalization can only be applied to entire xml documents.
        

