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

# tagSTRUCTURED_QUERY_SYNTAX enumeration


## -description


Specifies the type of query syntax. 


## -enum-fields




### -field SQS_NO_SYNTAX


        No syntax.
      


### -field SQS_ADVANCED_QUERY_SYNTAX


      Specifies the Advanced Query Syntax. For example, "kind:email to:david to:bill".
      


### -field SQS_NATURAL_QUERY_SYNTAX


      Specifies the Natural Query Syntax. This syntax removes the requirement for a colon between properties and values, for example, "email from david to bill".
      


## -remarks



Use this enumeration to set the desired SQSO_SYNTAX flag in <a href="https://msdn.microsoft.com/2753f0ad-2648-4ec2-b53f-089caad8ec15">STRUCTURED_QUERY_SINGLE_OPTION</a>, which is used with the methods <a href="https://msdn.microsoft.com/a7c2d4d7-7ccf-4daa-b4d5-cf23ed1e88b4">IQueryParser::SetOption</a> and <a href="https://msdn.microsoft.com/85216ad7-6988-43cd-87b3-49a2ca1173b6">IQueryParser::GetOption</a>.



