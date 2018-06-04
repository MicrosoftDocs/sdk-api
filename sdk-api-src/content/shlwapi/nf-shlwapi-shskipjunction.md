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

# SHSkipJunction function


## -description


Checks a bind context to see if it is safe to bind to a particular component object.


## -parameters




### -param pbc [in, optional]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> interface that specifies the bind context you want to check. This value can be <b>NULL</b>.


### -param pclsid [in]

Type: <b>const CLSID*</b>

A pointer to a variable that specifies the <b>CLSID</b> of the object being tested to see if it must be skipped. Typically, this is the CLSID of the object that <a href="https://msdn.microsoft.com/5e699494-1974-4b9b-8324-9394f7b96fe4">IShellFolder::BindToObject</a> is about to create.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the object specified by <i>pclsid</i> must be skipped, or <b>FALSE</b> otherwise.




## -remarks



This function can be used to avoid infinite cycles in namespace binding. For example, a folder shortcut that refers to a folder above it in the namespace tree can produce an infinitely recursive loop.



