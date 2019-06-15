---
UID: NS:webservices._WS_UNIQUE_ID_DESCRIPTION
title: WS_UNIQUE_ID_DESCRIPTION (webservices.h)
author: windows-sdk-content
description: An optional type description used with WS_UNIQUE_ID_TYPE to specify constraints on the set of values which can be deserialized.
old-location: wsw\ws_unique_id_description.htm
tech.root: wsw
ms.assetid: d00695e6-2c3d-4eff-b5cd-f4f81954fb0f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_UNIQUE_ID_DESCRIPTION, WS_UNIQUE_ID_DESCRIPTION structure [Web Services for Windows], webservices/WS_UNIQUE_ID_DESCRIPTION, wsw.ws_unique_id_description
ms.topic: struct
f1_keywords: ["webservices/WS_UNIQUE_ID_DESCRIPTION"]
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
 - WS_UNIQUE_ID_DESCRIPTION
product: Windows
targetos: Windows
req.typenames: WS_UNIQUE_ID_DESCRIPTION
req.redist: 
ms.custom: 19H1
---

# WS_UNIQUE_ID_DESCRIPTION structure


## -description


An optional type description used with <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_type">WS_UNIQUE_ID_TYPE</a> to specify constraints on the set of values
                which can be deserialized.
            


## -struct-fields




### -field minCharCount

The minimum number of characters.  This only pertains 
                    to the case where the unique ID is represented as a string.
                


### -field maxCharCount

The maximum number of characters.  This only pertains
                    to the case where the unique ID is represented as a string.
                

