---
UID: NF:ddraw.IDirectDrawClipper.Initialize
title: IDirectDrawClipper::Initialize (ddraw.h)
author: windows-sdk-content
description: Initializes a DirectDrawClipper object that was created by using the CoCreateInstance COM function.
old-location: directdraw\idirectdrawclipper_initialize.htm
tech.root: directdraw
ms.assetid: b0b71af4-f806-4264-bd14-b556b31aab29
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectDrawClipper interface [DirectDraw],Initialize method, IDirectDrawClipper.Initialize, IDirectDrawClipper::Initialize, Initialize, Initialize method [DirectDraw], Initialize method [DirectDraw],IDirectDrawClipper interface, ddraw/IDirectDrawClipper::Initialize, directdraw.idirectdrawclipper_initialize
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawClipper::Initialize


## -description


Initializes a DirectDrawClipper object that was created by using the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> COM function.



## -parameters




### -param arg1 [in]

A pointer to the DirectDraw object to associate with the DirectDrawClipper object. If this parameter is set to NULL, an independent DirectDrawClipper object is initialized; a call of this type is equivalent to using the <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-directdrawcreateclipper">DirectDrawCreateClipper</a> function. 



### -param arg2 [in]

Currently not used and must be set to 0.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_ALREADYINITIALIZED</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



The <b>IDirectDrawClipper::Initialize</b> method is provided for compliance with the Component Object Model (COM). If you used the <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-directdrawcreateclipper">DirectDrawCreateClipper</a> function or the <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-createclipper">IDirectDraw7::CreateClipper</a> method to create the DirectDrawClipper object, the <b>IDirectDrawClipper::Initialize</b> method returns DDERR_ALREADYINITIALIZED.

You must use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access the  <b>IDirectDrawClipper::Initialize</b> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nn-ddraw-idirectdrawclipper">IDirectDrawClipper</a>
 

 

