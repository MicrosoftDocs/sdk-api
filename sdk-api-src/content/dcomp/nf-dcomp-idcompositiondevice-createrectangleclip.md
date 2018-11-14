---
UID: NF:dcomp.IDCompositionDevice.CreateRectangleClip
title: IDCompositionDevice::CreateRectangleClip
author: windows-sdk-content
description: Creates a clip object that can be used to restrict the rendering of a visual subtree to a rectangular area.
old-location: directcomp\idcompositiondevice_createrectangleclip.htm
tech.root: directcomp
ms.assetid: b937fbf0-b920-413a-a184-ebe08ee893e5
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CreateRectangleClip, CreateRectangleClip method [DirectComposition], CreateRectangleClip method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateRectangleClip method, IDCompositionDevice.CreateRectangleClip, IDCompositionDevice::CreateRectangleClip, dcomp/IDCompositionDevice::CreateRectangleClip, directcomp.idcompositiondevice_createrectangleclip
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
 - IDCompositionDevice.CreateRectangleClip
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
- IDCompositionDevice.CreateRectangleClip
: 
---

# IDCompositionDevice::CreateRectangleClip


## -description


Creates a clip object that can be used to restrict the rendering of  a visual subtree to a rectangular area.


## -parameters




### -param clip [out]

Type: <b><a href="https://msdn.microsoft.com/486bcdb9-e353-4ca2-b24c-af863dda7470">IDCompositionRectangleClip</a>**</b>

The new clip object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A newly created clip object has a static value of <a href=" http://go.microsoft.com/fwlink/p/?linkid=200486">–FLT_MAX</a> for the left and top properties, and a static value of –FLT_MAX for the right and bottom properties, effectively making it a no-op clip object.




## -see-also




<a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a>



<a href="https://msdn.microsoft.com/ACEBA4F9-E1B0-459B-8DC2-272A822AB214">IDCompositionVisual::SetClip</a>
 

 

