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

# _FsrmTemplateApplyOptions enumeration


## -description


Defines the options for applying template changes to derived objects.


## -enum-fields




### -field FsrmTemplateApplyOptions_ApplyToDerivedMatching

Apply template changes to derived objects only if the object's properties match the template's properties.

Note that the comparison is made against the template as it exists in the database, not your local copy that 
       has not been committed yet.


### -field FsrmTemplateApplyOptions_ApplyToDerivedAll

Apply template changes to all derived objects, whether their properties match the template's or not.


## -see-also




<a href="https://msdn.microsoft.com/6b50a93f-f6f0-4ab4-a4a3-3995b721c5d7">IFsrmFileScreenTemplate::CommitAndUpdateDerived</a>



<a href="https://msdn.microsoft.com/fecb034f-3f11-4d37-9468-56d4ea6268e7">IFsrmQuotaTemplate::CommitAndUpdateDerived</a>
 

 

