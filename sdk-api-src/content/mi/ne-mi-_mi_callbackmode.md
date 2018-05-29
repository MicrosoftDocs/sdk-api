---
UID: NE:mi._MI_CallbackMode
title: "_MI_CallbackMode"
author: windows-sdk-content
description: Defines the callback mode for the CIM extensions for WriteError and PromptUser functions.
old-location: wmi_v2\mi_callbackmode.htm
old-project: wmi_v2
ms.assetid: 742610a4-3276-4bab-877d-8e74c6dc80cd
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_CALLBACKMODE_INQUIRE, MI_CALLBACKMODE_REPORT, MI_CallbackMode, MI_CallbackMode enumeration [Windows Management Infrastructure (MI)], _MI_CallbackMode, mi/MI_CALLBACKMODE_INQUIRE, mi/MI_CALLBACKMODE_REPORT, mi/MI_CallbackMode, wmi._mi_callbackmode, wmi_v2.mi_callbackmode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MI_CallbackMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_CallbackMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_CallbackMode enumeration


## -description


Defines the callback mode  for the CIM extensions for <b>WriteError</b> and <b>PromptUser</b> functions.


## -enum-fields




### -field MI_CALLBACKMODE_REPORT

Report the details to the client, but the provider will receive a preconfigured response.  The provider does not wait for the client to receive the request before continuing.


### -field MI_CALLBACKMODE_INQUIRE

Query the  client to determine whether  the provider should continue.


### -field MI_CALLBACKMODE_IGNORE



