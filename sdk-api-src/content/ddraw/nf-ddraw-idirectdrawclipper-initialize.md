---
UID: NF:ddraw.IDirectDrawClipper.Initialize
title: IDirectDrawClipper::Initialize
author: windows-sdk-content
description: Initializes a DirectDrawClipper object that was created by using the CoCreateInstance COM function.
old-location: directdraw\idirectdrawclipper_initialize.htm
old-project: directdraw
ms.assetid: b0b71af4-f806-4264-bd14-b556b31aab29
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: IDirectDrawClipper interface [DirectDraw],Initialize method, IDirectDrawClipper.Initialize, IDirectDrawClipper::Initialize, Initialize, Initialize method [DirectDraw], Initialize method [DirectDraw],IDirectDrawClipper interface, ddraw/IDirectDrawClipper::Initialize, directdraw.idirectdrawclipper_initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawClipper.Initialize
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawClipper::Initialize


## -description


Initializes a DirectDrawClipper object that was created by using the <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> COM function.



## -parameters




### -param






#### - dwFlags [in]

Currently not used and must be set to 0.


#### - lpDD [in]

A pointer to the DirectDraw object to associate with the DirectDrawClipper object. If this parameter is set to NULL, an independent DirectDrawClipper object is initialized; a call of this type is equivalent to using the <a href="https://msdn.microsoft.com/12d499d2-dd4a-4831-9290-c225aec1a160">DirectDrawCreateClipper</a> function. 



## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_ALREADYINITIALIZED</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



The <b>IDirectDrawClipper::Initialize</b> method is provided for compliance with the Component Object Model (COM). If you used the <a href="https://msdn.microsoft.com/12d499d2-dd4a-4831-9290-c225aec1a160">DirectDrawCreateClipper</a> function or the <a href="https://msdn.microsoft.com/123a07c0-d371-4d10-bff8-b5640bd3b920">IDirectDraw7::CreateClipper</a> method to create the DirectDrawClipper object, the <b>IDirectDrawClipper::Initialize</b> method returns DDERR_ALREADYINITIALIZED.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>IDirectDrawClipper::Initialize</b> method.




## -see-also




<a href="https://msdn.microsoft.com/2e93583a-59a8-4a0f-9299-ed57fdcebf33">IDirectDrawClipper</a>
 

 

