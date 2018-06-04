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

# IX509Enrollment2::get_RequestIdString


## -description


The <b>RequestIdString</b> property retrieves a string that contains a unique identifier for the certificate request sent to the certification enrollment server (CES).

This property is read-only.


## -parameters


## -remarks



The value of the <b>RequestIdString</b> property is set during the enrollment process. It can be used during subsequent communication between the client and the CES. For example, if a CES marks a request as pending when initially submitted, the client can use the request ID string when it again contacts the CES and attempts to retrieve the certificate response.




## -see-also




<a href="https://msdn.microsoft.com/8e262b4b-de6a-417e-9ade-0b451bd4c09a">IX509Enrollment2</a>
 

 

