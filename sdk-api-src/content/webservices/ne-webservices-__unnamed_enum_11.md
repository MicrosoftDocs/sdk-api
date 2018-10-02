---
UID: NE:webservices.__unnamed_enum_11
title: "__unnamed_enum_11"
author: windows-sdk-content
description: A set of flags used within a WS_OPERATION_DESCRIPTION structure.
old-location: wsw\ws_service_operation_message_option.htm
tech.root: wsw
ms.assetid: 3f54e012-4893-4f70-9f38-55ae9db365e8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_SERVICE_OPERATION_MESSAGE_NILLABLE_ELEMENT, WS_SERVICE_OPERATION_MESSAGE_OPTION, WS_SERVICE_OPERATION_MESSAGE_OPTION enumeration [Web Services for Windows], __unnamed_enum_11, webservices/WS_SERVICE_OPERATION_MESSAGE_NILLABLE_ELEMENT, webservices/WS_SERVICE_OPERATION_MESSAGE_OPTION, wsw.ws_service_operation_message_option
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: v.1.0
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
 - WS_SERVICE_OPERATION_MESSAGE_OPTION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# __unnamed_enum_11 enumeration


## -description


A set of flags used within a <a href="https://msdn.microsoft.com/d05b55aa-4159-4e48-ae75-2af36c0a7101">WS_OPERATION_DESCRIPTION</a> structure.
      


## -enum-fields




### -field WS_SERVICE_OPERATION_MESSAGE_NILLABLE_ELEMENT

This flag indicates that the message element may contain an xsi:nil attribute used to
          indicate a value which is nil. See the documentation for an individual
          <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a> to determine whether a nil value is supported for that type,
          and how nil is represented for that type.
        


## -remarks



For more information on which flag combinations are valid for which types,
        see the documentation for each individual <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a>.
      



