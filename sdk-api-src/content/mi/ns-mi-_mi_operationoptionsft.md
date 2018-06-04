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

