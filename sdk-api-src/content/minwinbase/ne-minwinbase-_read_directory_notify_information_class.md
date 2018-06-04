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

# _READ_DIRECTORY_NOTIFY_INFORMATION_CLASS enumeration


## -description


Indicates the possible types of information that an application that calls the <a href="https://msdn.microsoft.com/90C2F258-094C-4A0E-80E7-3FA241D288EA">ReadDirectoryChangesExW</a> function can request.


## -enum-fields




### -field ReadDirectoryNotifyInformation

The <a href="https://msdn.microsoft.com/90C2F258-094C-4A0E-80E7-3FA241D288EA">ReadDirectoryChangesExW</a> function  should provide  information that describes the changes within the specified directory, and return this information in the  output buffer in the form of <a href="https://msdn.microsoft.com/cb95352f-8a15-48d8-9150-e4bc395e0122">FILE_NOTIFY_INFORMATION</a> structures.


### -field ReadDirectoryNotifyExtendedInformation

The <a href="https://msdn.microsoft.com/90C2F258-094C-4A0E-80E7-3FA241D288EA">ReadDirectoryChangesExW</a> function  should provide  extended information that describes the changes within the specified directory, and return this information in the  output buffer in the form of <a href="https://msdn.microsoft.com/4558F2E8-F515-4202-9CAA-FDAF20160F61">FILE_NOTIFY_EXTENDED_INFORMATION</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/4558F2E8-F515-4202-9CAA-FDAF20160F61">FILE_NOTIFY_EXTENDED_INFORMATION</a>



<a href="https://msdn.microsoft.com/cb95352f-8a15-48d8-9150-e4bc395e0122">FILE_NOTIFY_INFORMATION</a>



<a href="https://msdn.microsoft.com/90C2F258-094C-4A0E-80E7-3FA241D288EA">ReadDirectoryChangesExW</a>
 

 

