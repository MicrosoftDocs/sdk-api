---
UID: NS:mi._MI_ApplicationFT
title: "_MI_ApplicationFT"
author: windows-sdk-content
description: A support structure used in the MI_Application structure. Use the functions with the name prefix &#0034;MI_Application_&#0034; to manipulate these structures.
old-location: wmi_v2\mi_applicationft.htm
old-project: wmi_v2
ms.assetid: 0c7d3902-a180-4d71-a223-8f8a68bc9d0b
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_ApplicationFT, MI_ApplicationFT structure [Windows Management Infrastructure (MI)], _MI_ApplicationFT, mi/MI_ApplicationFT, wmi_v2.mi_applicationft
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
req.typenames: MI_ApplicationFT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_ApplicationFT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_ApplicationFT structure


## -description


A support structure used in the 
     <a href="https://msdn.microsoft.com/da486ade-88ef-40c4-8151-356e718da7db">MI_Application</a> structure. Use the functions with the 
     name prefix "MI_Application_" to manipulate these structures.


## -struct-fields






#### - Close

Deinitializes the management infrastructure. See 
       <a href="https://msdn.microsoft.com/e5ad3ed3-8ef6-4bb5-999a-7d2ee91f51d5">MI_Application_Close</a>.


#### - NewDeserializer

Creates a deserializer that can be used to re-create the 
       <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> or 
       <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a>. See 
       <a href="https://msdn.microsoft.com/e58c69ce-032a-4024-9023-53cd1776b7f3">MI_Application_NewDeserializer</a>.


#### - NewDestinationOptions

Creates an <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object. 
       See <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>.


#### - NewHostedProvider

Creates a new hosted Provider. See 
       <a href="https://msdn.microsoft.com/4f39ffca-4ae3-4ce5-9460-c7ac27c06a50">MI_Application_NewHostedProvider</a>.


#### - NewInstance

Creates an instance. See 
       <a href="https://msdn.microsoft.com/e46adc55-c5dc-4395-b746-2ff13cc1e4bb">MI_Application_NewInstance</a>.


#### - NewOperationOptions

Creates an <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> object. See 
       <a href="https://msdn.microsoft.com/0b9f569b-bb32-4393-9fd2-9d5d601c2214">MI_Application_NewOperationOptions</a>.


#### - NewSerializer

Creates a serializer allowing a <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> or an 
       <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> to be persisted in a form that can be stored to 
       disk or transported over a transport. See 
       <a href="https://msdn.microsoft.com/9de29d43-0677-4dc9-927f-af7c01179991">MI_Application_NewSerializer</a>.


#### - NewSession

Creates a session that allows a group of operations that go to the same destination to be grouped so they 
       can share connections. See 
       <a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>.


#### - NewSubscriptionDeliveryOptions

See 
       <a href="https://msdn.microsoft.com/ac84ec09-7d91-42fc-8271-3e0e54bbb788">MI_Application_NewSubscriptionDeliveryOptions</a>.

