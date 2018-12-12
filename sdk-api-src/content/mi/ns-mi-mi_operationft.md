---
UID: NS:mi._MI_OperationFT
title: MI_OperationFT
author: windows-sdk-content
description: A support structure used in the MI_Operation structure. Use the functions with the name prefix &#0034;MI_Operation_&#0034; to manipulate these structures.
old-location: wmi_v2\mi_operationft.htm
tech.root: wmi_v2
ms.assetid: 925cd972-61fc-466d-a2a6-e315ef3fc499
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_OperationFT, MI_OperationFT structure [Windows Management Infrastructure (MI)], mi/MI_OperationFT, wmi_v2.mi_operationft
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
 - MI_OperationFT
product: Windows
targetos: Windows
req.typenames: MI_OperationFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_OperationFT structure


## -description


A support structure used in the <a href="https://msdn.microsoft.com/a62b3656-c281-4f30-9690-de453df9f2db">MI_Operation</a> 
     structure.  Use the functions with the name prefix "MI_Operation_" to manipulate these 
     structures.


## -struct-fields




### -field MI_Result

TBD 




#### - Cancel

Cancels a running operation. See 
       <a href="https://msdn.microsoft.com/11a9f9f6-9dfa-4f7c-9562-f4793c007f04">MI_Operation_Cancel</a>.


#### - Close

Closes an operation handle. See 
       <a href="https://msdn.microsoft.com/3e698e34-d537-4ea4-9345-cc4f493ff823">MI_Operation_Close</a>.


#### - GetClass

Closes an operation handle. See 
       <a href="https://msdn.microsoft.com/3e698e34-d537-4ea4-9345-cc4f493ff823">MI_Operation_Close</a>.


#### - GetIndication

Get the synchronous results from a subscription. See 
       <a href="https://msdn.microsoft.com/3e3e8472-ea33-485b-9e86-b5ba770af95b">MI_Operation_GetIndication</a>.


#### - GetInstance

Gets a synchronous result for an instance operation. See 
       <a href="https://msdn.microsoft.com/25c2d3fa-276d-4506-a044-4057c8cdc863">MI_Operation_GetInstance</a>.


#### - GetSession

Gets the session associated with an operation. See 
       <a href="https://msdn.microsoft.com/710ccbc5-956c-4bb3-b93b-f61a449c08ef">MI_Operation_GetSession</a>.

