---
UID: NS:wsman._WSMAN_ENVIRONMENT_VARIABLE
title: "_WSMAN_ENVIRONMENT_VARIABLE"
author: windows-sdk-content
description: Defines an individual environment variable by using a name and value pair.
old-location: winrm\wsman_environment_variable.htm
old-project: WinRM
ms.assetid: 0bf58de5-0c0b-4dc2-ba8b-c75e8201adc8
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSMAN_ENVIRONMENT_VARIABLE, WSMAN_ENVIRONMENT_VARIABLE structure [Windows Remote Management], _WSMAN_ENVIRONMENT_VARIABLE, winrm.wsman_environment_variable, wsman/WSMAN_ENVIRONMENT_VARIABLE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSMAN_ENVIRONMENT_VARIABLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wsman.h
api_name:
-	WSMAN_ENVIRONMENT_VARIABLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSMAN_ENVIRONMENT_VARIABLE structure


## -description


Defines an individual environment variable by using a name and value pair. This structure  is used by the <a href="https://msdn.microsoft.com/901c0a2d-d25f-451c-8d6c-83662f1f1061">WSManCreateShell</a> method. The representation of the <b>value</b> variable is shell specific. The client and server must  agree on the format of the <b>value</b> variable.


## -struct-fields




### -field name

Defines the environment variable name. This parameter cannot be <b>NULL</b>.


### -field value

Defines the environment variable value. <b>NULL</b> or empty string values are permitted.

