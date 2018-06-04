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

# tagVARDESC structure


## -description


Describes a variable, constant, or data member.


## -struct-fields




### -field memid

The member ID.


### -field lpstrSchema

Reserved.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.oInst

With VAR_PERINSTANCE, the offset of this variable within the instance.


### -field DUMMYUNIONNAME.lpvarValue

With VAR_CONST, the value of the constant.


### -field elemdescVar

The variable type.


### -field wVarFlags

The variable flags. See <a href="https://msdn.microsoft.com/9422f2a5-d8c0-4d65-ad7a-9eaa9bbedf91">VARFLAGS</a>.


### -field varkind

The variable type.

