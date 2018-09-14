---
UID: NS:webservices._WS_SECURITY_PROPERTIES
title: "_WS_SECURITY_PROPERTIES"
author: windows-sdk-content
description: Specifies an array of channel-wide security settings.
old-location: wsw\ws_security_properties.htm
tech.root: wsw
ms.assetid: 36a2dca5-d49f-4af7-ac1a-0ff7e9331e9a
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WS_SECURITY_PROPERTIES, WS_SECURITY_PROPERTIES structure [Web Services for Windows], _WS_SECURITY_PROPERTIES, webservices/WS_SECURITY_PROPERTIES, wsw.ws_security_properties
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
 - WS_SECURITY_PROPERTIES
product: Windows
targetos: Windows
req.typenames: WS_SECURITY_PROPERTIES
req.redist: 
---

# _WS_SECURITY_PROPERTIES structure


## -description


Specifies an array of channel-wide security settings.
      


## -struct-fields




### -field properties

An array of properties.  The number of elements in the array is specified
          using the propertyCount parameter.  This field may be <b>NULL</b> if the propertyCount
          is 0.
        


### -field propertyCount

The number of elements in the properties array.
        

