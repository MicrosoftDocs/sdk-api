---
UID: NS:mi._MI_OperationOptionsFT
title: "_MI_OperationOptionsFT"
author: windows-sdk-content
description: A support structure used in the MI_OperationOptions structure. Use the functions with the name prefix &#0034;MI_OperationOptions_&#0034; to manipulate these structures.
old-location: wmi_v2\mi_operationoptionsft.htm
tech.root: wmi_v2
ms.assetid: ed84d3bc-2cb0-4052-902d-96a3ab3a3ba4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MI_OperationOptionsFT, MI_OperationOptionsFT structure [Windows Management Infrastructure (MI)], _MI_OperationOptionsFT, mi/MI_OperationOptionsFT, wmi_v2.mi_operationoptionsft
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MI_OperationOptionsFT
product: Windows
targetos: Windows
req.typenames: MI_OperationOptionsFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# _MI_OperationOptionsFT structure


## -description


A support structure used in the <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.  Use the functions with the name prefix "MI_OperationOptions_" to manipulate these structures.


## -struct-fields






#### - Clone

Creates a copy of a <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure. See <a href="https://msdn.microsoft.com/22cce14f-55f0-4d31-a6cf-ea5e0a733d68">MI_OperationOptions_Clone</a>.


#### - Delete

Deletes an option and its associated memory. See <a href="https://msdn.microsoft.com/a9e43835-92a4-468a-9d45-1d4ab81d94f0">MI_OperationOptions_Delete</a>.


#### - GetEnabledChannels

See <a href="https://msdn.microsoft.com/5604288f-cc51-40b2-b9a8-5d972e05b172">MI_OperationOptions_GetEnabledChannels</a>.


#### - GetNumber

Gets a previously added custom number option. See <a href="https://msdn.microsoft.com/5c22c18d-9e1f-4cf7-84c1-e4e8863d0dc1">MI_OperationOptions_GetNumber</a>.


#### - GetOption

Gets a previously added option value based on the option name. See <a href="https://msdn.microsoft.com/bff6d5ee-9f13-4b54-8f33-4f73ce553c25">MI_OperationOptions_GetOption</a>.


#### - GetOptionAt

Gets a previously added option value based on the specified index. See <a href="https://msdn.microsoft.com/06ae674b-c7d7-47c1-81f2-6a825d9889a2">MI_OperationOptions_GetOptionAt</a>.


#### - GetOptionCount

Gets the number of options previously added. See <a href="https://msdn.microsoft.com/0c015ec7-d663-4207-b6d0-149da41cbf0e">MI_OperationOptions_GetOptionCount</a>.


#### - GetString

Gets a custom string option. See <a href="https://msdn.microsoft.com/1d1b9650-10c3-4e06-a841-6706ecc5f32c">MI_OperationOptions_GetString</a>.


#### - SetCustomOption

Sets a custom option for the operation. See <a href="https://msdn.microsoft.com/5db96e9e-dd81-4b62-a555-770b781d0ed3">MI_OperationOptions_SetCustomOption</a>.


#### - SetNumber

Sets a custom number option value. See <a href="https://msdn.microsoft.com/2f357a9c-7e61-4f78-b4cc-2dd0a8259c3d">MI_OperationOptions_SetNumber</a>.


#### - SetString

Sets a custom string option. See <a href="https://msdn.microsoft.com/1bfc3af0-cc43-4a80-acbe-010520acf8b5">MI_OperationOptions_SetString</a>.

