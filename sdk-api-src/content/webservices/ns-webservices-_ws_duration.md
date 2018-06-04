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

# _WS_DURATION structure


## -description



        Represents a <a href=" http://go.microsoft.com/fwlink/p/?linkid=139717">xsd:duration</a> data type.
      


## -struct-fields




### -field negative


          If <b>TRUE</b>, this represents a negative duration.
        


### -field years


          The number of years.
        


### -field months


          The number of months.
        


### -field days


          The number of days.
        


### -field hours


          The number of hours.
        


### -field minutes


          The number of minutes.
        


### -field seconds

The number of seconds.
        


### -field milliseconds

The number of milliseconds.  This value must be less than 1000.
        


### -field ticks


          Indicates the number of ticks.  This value must be less than 10000.
        

