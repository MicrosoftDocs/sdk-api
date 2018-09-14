---
UID: NS:webservices._WS_DURATION_DESCRIPTION
title: "_WS_DURATION_DESCRIPTION"
author: windows-sdk-content
description: An optional type description used with WS_DURATION_TYPE. It is used to specify constraints on the set of values which can be deserialized.
old-location: wsw\ws_duration_description.htm
tech.root: wsw
ms.assetid: 51084a56-f666-4ca0-b98c-9f41e28b99c0
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WS_DURATION_DESCRIPTION, WS_DURATION_DESCRIPTION structure [Web Services for Windows], _WS_DURATION_DESCRIPTION, webservices/WS_DURATION_DESCRIPTION, wsw.ws_duration_description
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_DURATION_DESCRIPTION
product: Windows
targetos: Windows
req.typenames: WS_DURATION_DESCRIPTION
req.redist: 
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
                

