---
UID: NS:webservices._WS_DATETIME_DESCRIPTION
title: "_WS_DATETIME_DESCRIPTION"
author: windows-sdk-content
description: This type description is used with WS_DATETIME_TYPE and is optional. It is used to specify constraints on the set of values which can be deserialized.
old-location: wsw\ws_datetime_description.htm
tech.root: wsw
ms.assetid: f6a7094f-56c0-4d8e-9050-fe41c4a82bf4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_DATETIME_DESCRIPTION, WS_DATETIME_DESCRIPTION structure [Web Services for Windows], _WS_DATETIME_DESCRIPTION, webservices/WS_DATETIME_DESCRIPTION, wsw.ws_datetime_description
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WS_DATETIME_DESCRIPTION
product: Windows
targetos: Windows
req.typenames: WS_DATETIME_DESCRIPTION
req.redist: 
---

# _WS_DATETIME_DESCRIPTION structure


## -description


This type description is used with <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_DATETIME_TYPE</a> and is optional.
                It is used to specify constraints on the set of values
                which can be deserialized.
            

Only the <b>ticks</b> member of the <a href="https://msdn.microsoft.com/635f8e0b-f994-4500-85ad-dd74fb4a6c22">WS_DATETIME</a> is compared.
            


## -struct-fields




### -field minValue

The minimum value.
                


### -field maxValue

The maximum value.
                

