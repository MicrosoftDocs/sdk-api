---
UID: NS:webservices._WS_DURATION
title: "_WS_DURATION"
author: windows-sdk-content
description: Represents a xsd:duration data type.
old-location: wsw\ws_duration.htm
old-project: wsw
ms.assetid: ccb08c23-8c6f-4ea7-a43b-c30a0df75805
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_DURATION, WS_DURATION structure [Web Services for Windows], _WS_DURATION, webservices/WS_DURATION, wsw.ws_duration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WS_DURATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_DURATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
        

