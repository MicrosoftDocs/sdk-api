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

# _WS_DURATION_DESCRIPTION structure


## -description



                An optional type description  used with <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_DURATION_TYPE</a>.
                It is used to specify constraints on the set of values
                which can be deserialized.
            


## -struct-fields




### -field minValue

The minimum value.
                


### -field maxValue


                    The maximum value.
                


### -field comparer


                    Specifies a function which can be used to compare <a href="https://msdn.microsoft.com/ccb08c23-8c6f-4ea7-a43b-c30a0df75805">WS_DURATION</a>. If <b>NULL</b>, a default
                    comparer is used.
                


                    Because <a href="https://msdn.microsoft.com/ccb08c23-8c6f-4ea7-a43b-c30a0df75805">WS_DURATION</a> has a partial ordering, not all durations can be unambiguously compared
                    (for example, 1 month and 30 days).  The default comparer function can compare durations that specify
                    years and months (but no other components), or durations that specify no years or months (but any other
                    component).
                

