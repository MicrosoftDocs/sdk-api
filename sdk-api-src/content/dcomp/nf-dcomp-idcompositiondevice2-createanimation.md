---
UID: NF:dcomp.IDCompositionDevice2.CreateAnimation
title: IDCompositionDevice2::CreateAnimation
author: windows-sdk-content
description: Creates an animation object that is used to animate one or more scalar properties of one or more Microsoft DirectComposition objects.
old-location: directcomp\idcompositiondevice2_createanimation.htm
tech.root: directcomp
ms.assetid: 6F15F6CD-E2EE-42E5-AF46-01A9A28F4896
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CreateAnimation, CreateAnimation method [DirectComposition], CreateAnimation method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateAnimation method, IDCompositionDevice2.CreateAnimation, IDCompositionDevice2::CreateAnimation, dcomp/IDCompositionDevice2::CreateAnimation, directcomp.idcompositiondevice2_createanimation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDCompositionDevice2.CreateAnimation
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
- IDCompositionDevice2.CreateAnimation
: 
---

# IDCompositionDevice2::CreateAnimation


## -description


Creates an animation object that is used to animate one or more scalar properties of one or more Microsoft DirectComposition objects.

  


## -parameters




### -param animation [out]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>**</b>

The new animation object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A number of DirectComposition object properties can have an animation object as the value of the property. When a property has an animation object as its value, DirectComposition redraws the visual at the refresh rate to reflect the changing value of the property that is being animated.

A newly created animation object does not have any animation segments associated with it. An application must use the methods of the <a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a> interface to build an animation function before setting the animation object as the property of another DirectComposition object.




## -see-also




<a href="https://msdn.microsoft.com/0E5D0AEC-63A3-4A44-9A0B-D1E26789CAB0">IDCompositionDevice2</a>
 

 

