---
UID: NS:wsman._WSMAN_ENVIRONMENT_VARIABLE_SET
title: "_WSMAN_ENVIRONMENT_VARIABLE_SET"
author: windows-sdk-content
description: Defines an array of environment variables.
old-location: winrm\wsman_environment_variable_set.htm
old-project: WinRM
ms.assetid: 3d9b4374-241f-489e-946a-9c180d77de3b
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSMAN_ENVIRONMENT_VARIABLE_SET, WSMAN_ENVIRONMENT_VARIABLE_SET structure [Windows Remote Management], _WSMAN_ENVIRONMENT_VARIABLE_SET, winrm.wsman_environment_variable_set, wsman/WSMAN_ENVIRONMENT_VARIABLE_SET
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
req.typenames: WSMAN_ENVIRONMENT_VARIABLE_SET
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSMAN_ENVIRONMENT_VARIABLE_SET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSMAN_ENVIRONMENT_VARIABLE_SET structure


## -description


Defines an array of environment variables.


## -struct-fields




### -field varsCount

Specifies the number of environment variables contained within the <b>vars</b> array.


### -field vars

Defines an array of environment variables. Each element of the array is of type <a href="https://msdn.microsoft.com/0bf58de5-0c0b-4dc2-ba8b-c75e8201adc8">WSMAN_ENVIRONMENT_VARIABLE</a>.

