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

# WS_DATETIME_FORMAT enumeration


## -description



        Specifies the textual format of a <a href="https://msdn.microsoft.com/635f8e0b-f994-4500-85ad-dd74fb4a6c22">WS_DATETIME</a>.
      


## -enum-fields




### -field WS_DATETIME_FORMAT_UTC


          This format displays a time in the GMT timezone.  It is formatted with a "Z" following the time.
          For example, September 25, 2007 at 1:30AM in the GMT timezone would be represented as "2007-09-25T01:30:00Z".
        


### -field WS_DATETIME_FORMAT_LOCAL


          This format displays a time with a specific timezone.  The time is followed by "[+|-]hh:mm" indicating the
          relative difference between the local time and UTC in hours and minutes.
          For example, September 27, 2007 at 10:30AM in the Pacific timezone would be represented as
          "2007-09-27T10:30:00-07:00".
        


          If the system is unable to convert the time to a local format because timezone information for the time
          specified it not available, then it will format the time as <a href="https://msdn.microsoft.com/e5859797-90dd-4509-ae41-f8d8c83cfd9c">WS_DATETIME_FORMAT_UTC</a>.
        


### -field WS_DATETIME_FORMAT_NONE


          This format displays a time with no timezone.  The time is formatted with no additional information and no
          timezone is implied.  For example, September 27, 2007 at 10:30AM would be represented as "2007-09-27T10:30:00".
        

