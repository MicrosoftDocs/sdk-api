---
UID: NF:objidl.IContext.RemoveProperty
title: IContext::RemoveProperty
author: windows-driver-content
description: Removes the specified context property from the context.
old-location: com\icontext_removeproperty.htm
old-project: com
ms.assetid: bb5b282a-d337-4371-b1c2-1b429a5bf135
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IContext interface [COM],RemoveProperty method, IContext.RemoveProperty, IContext::RemoveProperty, RemoveProperty, RemoveProperty method [COM], RemoveProperty method [COM],IContext interface, _com_icontext_removeproperty, com.icontext_removeproperty, objidlbase/IContext::RemoveProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	objidlbase.h
api_name:
-	IContext.RemoveProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IContext::RemoveProperty


## -description


Removes the specified context property from the context.


## -parameters




### -param rPolicyId [in]

The GUID that uniquely identifies the context property to be removed.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/89c41d9c-186c-4927-990d-92aa501f7d35">IContext</a>
 

 

