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

# CommitTemplateFlags enumeration


## -description


The <b>CommitTemplateFlags</b> enumeration type specifies options for saving and deleting templates. It is used by the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a> method on the <a href="https://msdn.microsoft.com/87660b16-06a8-4a71-8669-24521f1399e4">IX509CertificateTemplateWritable</a> interface.


## -enum-fields




### -field CommitFlagSaveTemplateGenerateOID

Save the template and create an object identifier for it.


### -field CommitFlagSaveTemplateUseCurrentOID

Not used.


### -field CommitFlagSaveTemplateOverwrite

Not used.


### -field CommitFlagDeleteTemplate

Delete the template.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a>



<a href="https://msdn.microsoft.com/87660b16-06a8-4a71-8669-24521f1399e4">IX509CertificateTemplateWritable</a>
 

 

