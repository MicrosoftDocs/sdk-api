---
UID: NF:dcomp.IDCompositionTarget.SetRoot
title: IDCompositionTarget::SetRoot
author: windows-sdk-content
description: Sets a visual object as the new root object of a visual tree.
old-location: directcomp\idcompositiontarget_setroot.htm
tech.root: directcomp
ms.assetid: febbef70-fc21-4295-93c5-2f9f52434aae
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDCompositionTarget interface [DirectComposition],SetRoot method, IDCompositionTarget.SetRoot, IDCompositionTarget::SetRoot, SetRoot, SetRoot method [DirectComposition], SetRoot method [DirectComposition],IDCompositionTarget interface, dcomp/IDCompositionTarget::SetRoot, directcomp.idcompositiontarget_setroot
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
 - IDCompositionTarget.SetRoot
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dcomp.h
: 
- IDCompositionTarget.SetRoot
: 
---

# IDCompositionTarget::SetRoot


## -description


Sets a visual object as the new root object of a visual tree.


## -parameters




### -param visual [in, optional]

Type: <b><a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>*</b>

The visual object that is the new root of this visual tree. This parameter can be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A visual can be either the root of a single visual tree, or a child of another visual, but it cannot be both at the same time. This method fails if the <i>visual</i> parameter is already the root of another visual tree, or is a child of another visual.

If <i>visual</i> is NULL, the visual tree is empty. If there was a previous non-NULL root visual, that visual becomes available for use as the root of another visual tree, or as a child of another visual.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/86006C3C-67A8-4931-BE76-D0CA9DB19505">How to Build a Simple Visual Tree</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3b4fefe0-772e-42bd-8e81-37d0b128c418">IDCompositionDevice::CreateVisual</a>



<a href="https://msdn.microsoft.com/86dbfe68-e360-42cf-b572-960398ef06ba">IDCompositionTarget</a>
 

 

