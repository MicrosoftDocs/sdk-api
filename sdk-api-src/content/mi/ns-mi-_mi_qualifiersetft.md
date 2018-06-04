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

# _MI_QualifierSetFT structure


## -description


A support structure used in the 
     <a href="https://msdn.microsoft.com/6c374d19-c433-4c70-a644-e53a401f96dd">MI_QualifierSet</a> structure. Use the functions with the 
     name prefix "MI_QualifierSet_" to manipulate these structures.


## -struct-fields






#### - GetQualifier

Gets a named qualifier. See 
       <a href="https://msdn.microsoft.com/16dde421-3746-4722-9f08-56835b7603fb">MI_QualifierSet_GetQualifier</a>.


#### - GetQualifierAt

Gets a qualifier at the specified index. See 
       <a href="https://msdn.microsoft.com/5dfcdd7a-7740-4d40-b412-89f6f090561c">MI_QualifierSet_GetQualifierAt</a>.


#### - GetQualifierCount

Gets the number of qualifiers in a qualifier set. See 
       <a href="https://msdn.microsoft.com/0027b8fc-0528-4aa8-85bc-088429e1e045">MI_QualifierSet_GetQualifierCount</a>.

