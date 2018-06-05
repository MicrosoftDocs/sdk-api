---
UID: NS:mi._MI_DestinationOptionsFT
title: "_MI_DestinationOptionsFT"
author: windows-sdk-content
description: A support structure used in the MI_DestinationOptions structure. Use the functions with the name prefix &#0034;MI_DestinationOptions_&#0034; to manipulate these structures.
old-location: wmi_v2\mi_destinationoptionsft.htm
old-project: wmi_v2
ms.assetid: e6cf4d82-8820-40d5-924a-e4270252807d
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_DestinationOptionsFT, MI_DestinationOptionsFT structure [Windows Management Infrastructure (MI)], _MI_DestinationOptionsFT, mi/MI_DestinationOptionsFT, wmi_v2.mi_destinationoptionsft
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
tech.root: 
req.typenames: MI_DestinationOptionsFT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_DestinationOptionsFT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_DestinationOptionsFT structure


## -description


A support structure used in the <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> structure.  Use the functions with the name prefix "MI_DestinationOptions_" to manipulate these structures.


## -struct-fields






#### - AddCredentials

Used internally.


#### - Clone

Creates a copy of a <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> structure. See <a href="https://msdn.microsoft.com/f331561b-97ad-42f1-91b3-d180db92da07">MI_DestinationOptions_Clone</a>.


#### - Delete

Deletes the destination options created by using <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>. See <a href="https://msdn.microsoft.com/c4cc8622-1adb-4e91-877f-11a260ca4bd7">MI_DestinationOptions_Delete</a>.


#### - GetCredentialsAt

Get the credentials at the specified index. See <a href="https://msdn.microsoft.com/605f6486-f7d4-433e-9f56-49a868de9e8e">MI_DestinationOptions_GetCredentialsAt</a>.


#### - GetCredentialsCount

Gets the number of previously added credentials. See <a href="https://msdn.microsoft.com/65262f1d-19fc-49bc-a5e3-0d579185c1af">MI_DestinationOptions_GetCredentialsCount</a>.


#### - GetCredentialsPasswordAt

Gets a credentials password based on a specified index. See <a href="https://msdn.microsoft.com/95ea5856-5b15-4522-9652-a7b52d89055a">MI_DestinationOptions_GetCredentialsPasswordAt</a>.


#### - GetNumber

Gets a previously added custom number option. See <a href="https://msdn.microsoft.com/ac48c290-631f-427e-a544-ee0258029c42">MI_DestinationOptions_GetNumber</a>.


#### - GetOption

Gets a previously added option value based on the option name. See <a href="https://msdn.microsoft.com/f7f26a4f-109f-4169-bc77-b0c763d7bcb8">MI_DestinationOptions_GetOption</a>.


#### - GetOptionAt

Gets a previously added option value based on the specified index. See <a href="https://msdn.microsoft.com/8705721f-3631-4a92-aa5b-0f1b196fe684">MI_DestinationOptions_GetOptionAt</a>.


#### - GetOptionCount

Gets the number of options previously added. See <a href="https://msdn.microsoft.com/8bfbd58d-3c9d-4828-9922-ba13033a6c96">MI_DestinationOptions_GetOptionCount</a>.


#### - GetString

Gets a previously added custom string option. See <a href="https://msdn.microsoft.com/49bd7fa6-0164-4fb6-8154-75c39e6f7858">MI_DestinationOptions_GetString</a>.


#### - SetNumber

Sets a custom numeric option value. See <a href="https://msdn.microsoft.com/46e81ecd-7fb5-465a-8caa-04288c559fea">MI_DestinationOptions_SetNumber</a>.


#### - SetString

Sets a custom string option. See <a href="https://msdn.microsoft.com/40621d0b-3ff2-4960-8cb0-e95bad0d08db">MI_DestinationOptions_SetString</a>.

