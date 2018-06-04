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

# _WS_XML_READER_STREAM_INPUT structure


## -description



        Specifies that the source of the xml should be obtained from a callback.
      


## -struct-fields




### -field input


          The base type for all types that derive from <a href="https://msdn.microsoft.com/1e7a708d-5dcf-44ec-b781-a34946cb2844">WS_XML_READER_INPUT</a>.
        


### -field readCallback

A callback that is invoked when <a href="https://msdn.microsoft.com/1f4138a2-acc5-4f1d-8e35-544859d2fa49">WsFillReader</a> is called.
        


### -field readCallbackState


          A user-defined value that will be passed back to readCallback.
        

