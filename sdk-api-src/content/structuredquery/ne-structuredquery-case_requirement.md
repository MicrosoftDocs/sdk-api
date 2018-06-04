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

# CASE_REQUIREMENT enumeration


## -description


Specifies the case requirements of keywords, if any, for a query. 


## -enum-fields




### -field CASE_REQUIREMENT_ANY


        Keywords are recognized regardless of case.
      


### -field CASE_REQUIREMENT_UPPER_IF_AQS


      	Keywords are recognized only if uppercase when AQS is the syntax. When AQS is not the syntax, keywords are recognized regardless of case.
      


## -remarks



Keywords include Boolean operators such as AND, NOT, and OR.




## -see-also




<a href="https://msdn.microsoft.com/84a052ae-4d05-438f-ab90-e1a248239aca">STRUCTURED_QUERY_RESOLVE_OPTION</a>
 

 

