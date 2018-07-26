---
UID: NF:directmanipulation.IDirectManipulationManager2.CreateBehavior
title: IDirectManipulationManager2::CreateBehavior
author: windows-sdk-content
description: Factory method to create a behavior.
old-location: directmanipulation\idirectmanipulationmanager2_createbehavior.htm
old-project: directmanipulation
ms.assetid: 8890E44F-595A-4116-B4A4-F10FAEE598B7
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: CreateBehavior, CreateBehavior method [Direct Manipulation], CreateBehavior method [Direct Manipulation],IDirectManipulationManager2 interface, IDirectManipulationManager2 interface [Direct Manipulation],CreateBehavior method, IDirectManipulationManager2.CreateBehavior, IDirectManipulationManager2::CreateBehavior, directmanipulation.idirectmanipulationmanager2_createbehavior, directmanipulation/IDirectManipulationManager2::CreateBehavior
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationManager2.CreateBehavior
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationManager2::CreateBehavior


## -description


Factory method to create a behavior.


## -parameters




### -param clsid [in]

CLSID of the behavior. The CLSID specifies the type of behavior.


### -param riid [in]

The IID of the behavior interface to create.


### -param object [out, retval]

The new behavior object that implements the specified interface.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/094C6C7D-F973-45AC-9B83-43DB9D46AF23">IDirectManipulationManager2</a>
 

 

