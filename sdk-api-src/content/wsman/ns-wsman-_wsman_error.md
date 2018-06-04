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

# _WSMAN_ERROR structure


## -description


Contains error information that is returned by a Windows Remote Management (WinRM) client. The <a href="https://msdn.microsoft.com/72d05ef9-672c-4693-b7c9-6d689858acd4">WSMAN_ERROR</a> structure is used by all callbacks to return error information and is valid only for the callback.


## -struct-fields




### -field code

Specifies an error code. This error can be a general error code that is defined in winerror.h or a WinRM-specific error code.


### -field errorDetail

Specifies extended error information that relates to a failed call. This field contains the fault detail text if it is present in the fault. If there is no fault detail, this field contains the fault reason text. This field can be set to <b>NULL</b>.


### -field language

Specifies the language for the error description. This field can be set to <b>NULL</b>.  For more information about the language format, see the    RFC 3066 specification from the Internet Engineering Task Force at <a href="http://go.microsoft.com/fwlink/p/?linkid=139708">http://www.ietf.org/rfc/rfc3066.txt</a>.


### -field machineName

Specifies the name of the computer. This field can be set to <b>NULL</b>.


### -field pluginName

Specifies the name of the plug-in that generated the error. This field can be set to <b>NULL</b>.

