---
UID: NE:objidl.tagSERVERCALL
title: tagSERVERCALL
author: windows-sdk-content
description: Indicates the status of server call.
old-location: com\servercall.htm
tech.root: com
ms.assetid: 2a9b5e85-44b9-43c1-b3e5-a8f2c140b674
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: SERVERCALL, SERVERCALL enumeration [COM], SERVERCALL_ISHANDLED, SERVERCALL_REJECTED, SERVERCALL_RETRYLATER, _com_SERVERCALL, com.servercall, objidl/SERVERCALL, objidl/SERVERCALL_ISHANDLED, objidl/SERVERCALL_REJECTED, objidl/SERVERCALL_RETRYLATER, tagSERVERCALL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Objidl.h
api_name:
 - SERVERCALL
product: Windows
targetos: Windows
req.typenames: SERVERCALL
req.redist: 
---

# tagSERVERCALL enumeration


## -description


Indicates the status of server call.


## -enum-fields




### -field SERVERCALL_ISHANDLED

The object may be able to process the call.


### -field SERVERCALL_REJECTED

The object cannot handle the call due to an unforeseen problem, such as network unavailability.


### -field SERVERCALL_RETRYLATER

The object cannot handle the call at this time. For example, an application might return this value when it is in a user-controlled modal state.


## -see-also




<a href="https://msdn.microsoft.com/7e31b518-ef4f-4bdd-b5c7-e1b16383a5be">IMessageFilter::HandleInComingCall</a>



<a href="https://msdn.microsoft.com/3f800819-2a21-4e46-ad15-f9594fac1a3d">IMessageFilter::RetryRejectedCall</a>
 

 

