---
UID: NF:radialcontrollerinterop.IRadialControllerInterop.CreateForWindow
title: IRadialControllerInterop::CreateForWindow method
author: windows-driver-content
description: Instantiates a RadialController object and binds it to the active application.
old-location: input_radial\iradialcontrollerinterop_createforwindow.htm
old-project: Input_Radial
ms.assetid: fe419ce2-9767-42c4-aaa6-a9b9ea93ec3e
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CreateForWindow method, CreateForWindow method, IRadialControllerInterop interface, CreateForWindow,IRadialControllerInterop.CreateForWindow, IRadialControllerInterop, IRadialControllerInterop interface, CreateForWindow method, IRadialControllerInterop::CreateForWindow, Input_Radial.iradialcontrollerinterop_createforwindow, radialcontrollerinterop/IRadialControllerInterop::CreateForWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: radialcontrollerinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RadialControllerInterop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RSVP_STATUS_INFO, *LPRSVP_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RadialControllerInterop.h
api_name:
-	IRadialControllerInterop.CreateForWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRadialControllerInterop::CreateForWindow method


## -description


Instantiates a <a href="https://msdn.microsoft.com/5cd9534d-bdd7-49fa-81c7-a5ddca4e851a">RadialController</a> object and binds it to the active application.


## -parameters




### -param hwnd [in]

Handle to the window of the active application.


### -param riid [in]

The GUID for the resource interface.

The REFIID, or GUID, of the interface to the resource can be obtained by using the __uuidof() macro. For example, __uuidof(IRadialController) will get the GUID of the interface to a buffer resource.


### -param ppv [out]

Address of a pointer to a <a href="https://msdn.microsoft.com/5cd9534d-bdd7-49fa-81c7-a5ddca4e851a">RadialController</a> object.


## -returns



If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<b>Developer and UX guidance</b>



<a href="https://msdn.microsoft.com/ed701930-fae7-4c42-9e6b-b1cb3fac861c">IRadialControllerInterop</a>



<b>Samples</b>



<a href="https://go.microsoft.com/fwlink/?linkid=832322">Surface Dial interactions</a>



<a href="https://go.microsoft.com/fwlink/?linkid=832713">Universal Windows Platform samples (C# and C++)</a>



<a href="https://aka.ms/radialcontrollerclassicsample">Windows classic desktop sample</a>
 

 

