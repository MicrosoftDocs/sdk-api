---
UID: NF:dcomp.IDCompositionDevice.CreateVisual
title: IDCompositionDevice::CreateVisual
author: windows-sdk-content
description: Creates a new visual object.
old-location: directcomp\idcompositiondevice_createvisual.htm
tech.root: directcomp
ms.assetid: 3b4fefe0-772e-42bd-8e81-37d0b128c418
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CreateVisual, CreateVisual method [DirectComposition], CreateVisual method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateVisual method, IDCompositionDevice.CreateVisual, IDCompositionDevice::CreateVisual, dcomp/IDCompositionDevice::CreateVisual, directcomp.idcompositiondevice_createvisual
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDevice.CreateVisual
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice::CreateVisual


## -description


Creates a new visual object.


## -parameters




### -param visual [out]

Type: <b><a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>**</b>

The new visual object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A new visual object has a static value of zero for the OffsetX and OffsetY properties, and NULL for the Transform, Clip, and Content properties. Initially, the visual  does not cause the contents of a window to change. The visual must be added as a child of another visual, or as the root of a composition target, before it can affect the appearance of a window.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/86006C3C-67A8-4931-BE76-D0CA9DB19505">How to Build a Simple Visual Tree</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a>



<a href="https://msdn.microsoft.com/febbef70-fc21-4295-93c5-2f9f52434aae">IDCompositionTarget::SetRoot</a>



<a href="https://msdn.microsoft.com/e1124df5-7795-49c3-a640-f218cfdd4f1d">IDCompositionVisual::AddVisual</a>
 

 

