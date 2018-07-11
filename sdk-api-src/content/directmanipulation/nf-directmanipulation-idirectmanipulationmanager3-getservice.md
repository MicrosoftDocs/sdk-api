---
UID: NF:directmanipulation.IDirectManipulationManager3.GetService
title: IDirectManipulationManager3::GetService
author: windows-sdk-content
description: Retrieves an IDirectManipulationDeferContactService object.
old-location: directmanipulation\idirectmanipulationmanager3_getservice.htm
old-project: directmanipulation
ms.assetid: 36f46402-ed71-41d8-8df5-02ef59819bb3
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetService, GetService method [Direct Manipulation], GetService method [Direct Manipulation],IDirectManipulationManager3 interface, IDirectManipulationManager3 interface [Direct Manipulation],GetService method, IDirectManipulationManager3.GetService, IDirectManipulationManager3::GetService, directmanipulation.idirectmanipulationmanager3_getservice, directmanipulation/IDirectManipulationManager3::GetService
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDirectManipulationManager3.GetService
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationManager3::GetService


## -description


Retrieves an <a href="https://msdn.microsoft.com/6063352F-39FF-4E8F-B836-3DA0A02BE523">IDirectManipulationDeferContactService</a> object.


## -parameters




### -param clsid [in]

 The <a href="https://msdn.microsoft.com/6063352F-39FF-4E8F-B836-3DA0A02BE523">IDirectManipulationDeferContactService</a> CLSID. 


### -param riid [in]

The IID of the <a href="https://msdn.microsoft.com/6063352F-39FF-4E8F-B836-3DA0A02BE523">IDirectManipulationDeferContactService</a> to retrieve.


### -param object [out, retval]

The <a href="https://msdn.microsoft.com/6063352F-39FF-4E8F-B836-3DA0A02BE523">IDirectManipulationDeferContactService</a> object.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/566d4a36-5623-4896-b23b-3824551850b0">IDirectManipulationManager3</a>
 

 

