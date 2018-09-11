---
UID: NS:mi._MI_ParameterSetFT
title: "_MI_ParameterSetFT"
author: windows-sdk-content
description: A support structure used in the MI_ParameterSet structure. Use the functions with the name prefix MI_ParameterSet_ to manipulate these structures.
old-location: wmi_v2\mi_parametersetft.htm
tech.root: wmi_v2
ms.assetid: 48e10e9c-8e50-4811-bd2a-1934d27373f0
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: MI_ParameterSetFT, MI_ParameterSetFT structure [Windows Management Infrastructure (MI)], _MI_ParameterSetFT, mi/MI_ParameterSetFT, wmi_v2.mi_parametersetft
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_ParameterSetFT
product: Windows
targetos: Windows
req.typenames: MI_ParameterSetFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# _MI_ParameterSetFT structure


## -description


A support structure used in the <a href="https://msdn.microsoft.com/14b5773c-4741-453b-824a-226aab9b8a10">MI_ParameterSet</a> structure.  Use the functions with the name prefix MI_ParameterSet_ to manipulate these structures.


## -struct-fields






#### - GetMethodReturnType

Gets the method return type and qualifier set for a specified parameter set. See <a href="https://msdn.microsoft.com/8d2e881a-72a8-4819-a407-b7381ab7a94a">MI_ParameterSet_GetMethodReturnType</a>.


#### - GetParameter

Gets a method's parameter information based on a parameter name. See <a href="https://msdn.microsoft.com/ff895beb-8354-488d-9c97-2d0448da954a">MI_ParameterSet_GetParameter</a>.


#### - GetParameterAt

Gets a method's parameter information at the specified index. See <a href="https://msdn.microsoft.com/fcfd7104-dd63-4a48-9a20-dcec0dc33242">MI_ParameterSet_GetParameterAt</a>.


#### - GetParameterCount

Gets the number of parameters in a parameter set. See <a href="https://msdn.microsoft.com/4b1ca06f-426c-483f-a571-b49eb06991e1">MI_ParameterSet_GetParameterCount</a>.

