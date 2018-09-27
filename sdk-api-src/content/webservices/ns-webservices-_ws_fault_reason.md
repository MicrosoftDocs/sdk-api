---
UID: NS:webservices._WS_FAULT_REASON
title: "_WS_FAULT_REASON"
author: windows-sdk-content
description: Contains an explanation of the fault.
old-location: wsw\ws_fault_reason.htm
tech.root: wsw
ms.assetid: 70ec3d18-00ab-4dde-8a8a-b200eda44acd
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: WS_FAULT_REASON, WS_FAULT_REASON structure [Web Services for Windows], _WS_FAULT_REASON, webservices/WS_FAULT_REASON, wsw.ws_fault_reason
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - WS_FAULT_REASON
product: Windows
targetos: Windows
req.typenames: WS_FAULT_REASON
req.redist: 
---

# _WS_FAULT_REASON structure


## -description


Contains an explanation of the fault.


## -struct-fields




### -field text

Text describing the fault.
                


### -field lang

The language identifier that identifies the language of the text.
                

The identifier is serialized using the xml:lang attribute, and has
                    values that follow <a href="http://go.microsoft.com/fwlink/p/?linkid=139708">RFC3066.txt</a>. 
                

