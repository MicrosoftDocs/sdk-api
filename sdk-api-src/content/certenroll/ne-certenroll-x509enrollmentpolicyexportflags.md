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

# X509EnrollmentPolicyExportFlags enumeration


## -description


The <b>X509EnrollmentPolicyExportFlags</b> enumeration is used by the <a href="https://msdn.microsoft.com/b821329b-2ec6-4f47-ba5f-2e1cd7ffb06f">Export</a> method on the <a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a> interface to specify what items to export from the policy server.


## -enum-fields




### -field ExportTemplates

Export templates.


### -field ExportOIDs

Export custom object identifiers.


### -field ExportCAs

Not used.


## -remarks



To export both templates and object identifiers, specify a bitwise <b>OR</b> of the <b>ExportTemplates</b> and <b>ExportOIDs</b> values.




## -see-also




<a href="https://msdn.microsoft.com/b821329b-2ec6-4f47-ba5f-2e1cd7ffb06f">Export</a>
 

 

