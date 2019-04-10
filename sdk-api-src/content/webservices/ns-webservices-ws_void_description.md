---
UID: NS:webservices._WS_VOID_DESCRIPTION
title: WS_VOID_DESCRIPTION (webservices.h)
author: windows-sdk-content
description: Specifies information about a field which is neither serialized nor deserialized.
old-location: wsw\ws_void_description.htm
tech.root: wsw
ms.assetid: 92373e0d-3fe1-4486-8e79-deb0fc24cb63
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_VOID_DESCRIPTION, WS_VOID_DESCRIPTION structure [Web Services for Windows], webservices/WS_VOID_DESCRIPTION, wsw.ws_void_description
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
 - WS_VOID_DESCRIPTION
product: Windows
targetos: Windows
req.typenames: WS_VOID_DESCRIPTION
req.redist: 
---

# WS_VOID_DESCRIPTION structure


## -description


Specifies information about a field which is neither serialized nor
                deserialized.
            

This is used with <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_VOID_TYPE</a> and <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>within a <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a>.
            

This type description is only required when <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> is not
                being used.
            


## -struct-fields




### -field size

The size of the field.
                

