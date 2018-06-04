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

# WebEnrollmentFlags enumeration


## -description


The <b>WebEnrollmentFlags</b> enumeration specifies web enrollment behavior. It is used by the <a href="https://msdn.microsoft.com/4f178df7-714f-49e6-9bf5-647acc23b0ad">Enroll</a> method on the <a href="https://msdn.microsoft.com/19124591-be1a-401e-9b83-c640d00de34a">IX509EnrollmentHelper</a> interface.


## -enum-fields




### -field EnrollPrompt

If this flag is set and no authentication credential is available for the certificate enrollment server, the certificate service prompts for a credential. If there is no authentication credential and this flag is not set, the <a href="https://msdn.microsoft.com/4f178df7-714f-49e6-9bf5-647acc23b0ad">Enroll</a> method fails.


## -see-also




<a href="https://msdn.microsoft.com/4f178df7-714f-49e6-9bf5-647acc23b0ad">Enroll</a>



<a href="https://msdn.microsoft.com/19124591-be1a-401e-9b83-c640d00de34a">IX509EnrollmentHelper</a>
 

 

