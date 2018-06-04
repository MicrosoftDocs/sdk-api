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

# __MIDL_IAssemblyName_0004 enumeration


## -description


The values of the <b>ASM_CMP_FLAGS</b> enumeration are used by the <a href="https://msdn.microsoft.com/library/windows/hardware/dn926880">IsEqual</a> method to specify which portions of two assembly names to compare.


## -enum-fields




### -field ASM_CMPF_NAME

Compare the name portion of the assembly names.


### -field ASM_CMPF_MAJOR_VERSION

Compare the major version portion of the assembly names.


### -field ASM_CMPF_MINOR_VERSION

Compare the minor version portion of the assembly names.


### -field ASM_CMPF_BUILD_NUMBER

Compare the build version portion of the assembly names.


### -field ASM_CMPF_REVISION_NUMBER

Compare the revision version portion of the assembly names.


### -field ASM_CMPF_PUBLIC_KEY_TOKEN

Compare the public key token portion of the assembly names.


### -field ASM_CMPF_CULTURE

Compare the culture portion of the assembly names.


### -field ASM_CMPF_CUSTOM

Compare the custom portion of the assembly names.


### -field ASM_CMPF_ALL

Compare all portions of the assembly names. This is equivalent to setting:

ASM_CMPF_NAME | ASM_CMPF_MAJOR_VERSION | ASM_CMPF_MINOR_VERSION | ASM_CMPF_REVISION_NUMBER | ASM_CMPF_BUILD_NUMBER | ASM_CMPF_PUBLIC_KEY_TOKEN | ASM_CMPF_CULTURE | ASM_CMPF_CUSTOM


### -field ASM_CMPF_DEFAULT

 Ignore the version number to compare assemblies with simple names.

