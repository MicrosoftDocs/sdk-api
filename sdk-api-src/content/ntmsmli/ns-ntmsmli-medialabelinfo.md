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

# MediaLabelInfo structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>MediaLabelInfo</b> structure conveys information to the RSM database about a tape OMID. The media label library fills in this structure for all media labels the library recognizes.


## -struct-fields




### -field LabelType

Unicode string that identifies the source of the media label. Often this is the name of the backup application or Windows command that wrote the label,
for example, "Microsoft Windows Wbadmin".


### -field LabelIDSize

Number of bytes that are used in the <b>LabelID</b> member.


### -field LabelID

Unique identifier for the media label.


### -field LabelAppDescr

Unicode string that describes the media. For example, the description for a backup media label would be similar to "Tape created on 04/14/97".


## -see-also




<a href="https://msdn.microsoft.com/ac957769-0513-436b-94f0-e3894f7a703b">ClaimMediaLabel</a>
 

 

