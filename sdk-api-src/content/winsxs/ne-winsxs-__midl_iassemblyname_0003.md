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

# __MIDL_IAssemblyName_0003 enumeration


## -description


The values of the  <b>ASM_DISPLAY_FLAGS</b> enumeration are used by the <a href="https://msdn.microsoft.com/d2d74d67-a893-4f2f-8161-80bf3d5cbedb">GetDisplayName</a> method to specify which portions of the assembly's full name to include in the string representation of the assembly name.


## -enum-fields




### -field ASM_DISPLAYF_VERSION

Include the version number.


### -field ASM_DISPLAYF_CULTURE

Include the culture.


### -field ASM_DISPLAYF_PUBLIC_KEY_TOKEN

Include the public key token.


### -field ASM_DISPLAYF_PUBLIC_KEY

Include the public key.


### -field ASM_DISPLAYF_CUSTOM

Include the custom part of the assembly name.


### -field ASM_DISPLAYF_PROCESSORARCHITECTURE

Include the processor architecture.


### -field ASM_DISPLAYF_LANGUAGEID

Reserved.

