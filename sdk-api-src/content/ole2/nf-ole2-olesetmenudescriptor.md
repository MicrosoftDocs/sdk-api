---
UID: NF:ole2.OleSetMenuDescriptor
title: OleSetMenuDescriptor function
author: windows-sdk-content
description: Installs or removes OLE dispatching code from the container's frame window.
old-location: com\olesetmenudescriptor.htm
old-project: com
ms.assetid: c80fe36d-5093-4814-83a9-0c11c5a7cf5f
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: OleSetMenuDescriptor, OleSetMenuDescriptor function [COM], _ole_OleSetMenuDescriptor, com.olesetmenudescriptor, ole2/OleSetMenuDescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: QACONTROL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
api_name:
-	OleSetMenuDescriptor
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OleSetMenuDescriptor function


## -description


Installs or removes OLE dispatching code from the container's frame window.




## -parameters




### -param holemenu [in]

Handle to the composite menu descriptor returned by the <a href="https://msdn.microsoft.com/b4a6b3f1-aee9-4b68-8ffe-24bd497db0a0">OleCreateMenuDescriptor</a> function. If <b>NULL</b>, the dispatching code is unhooked.


### -param hwndFrame [in]

 Handle to the container's frame window where the in-place composite menu is to be installed.


### -param hwndActiveObject [in]

Handle to the object's in-place activation window. OLE dispatches menu messages and commands to this window.


### -param lpFrame [in]

Pointer to the <a href="https://msdn.microsoft.com/c530aff7-fd83-413d-8945-0c9d1bfb51ba">IOleInPlaceFrame</a> interface on the container's frame window.


### -param lpActiveObj [in]

Pointer to the <a href="https://msdn.microsoft.com/b077c256-1109-494c-95c2-2d33bccbe47b">IOleInPlaceActiveObject</a> interface on the active in-place object.


## -returns



This function returns S_OK on success.




## -remarks



The container should call <b>OleSetMenuDescriptor</b> to install the dispatching code on <i>hwndFrame</i> when the object calls the <a href="https://msdn.microsoft.com/dc26a399-846d-4d15-b406-752350e528c2">IOleInPlaceFrame::SetMenu</a> method, or to remove the dispatching code by passing <b>NULL</b> as the value for <i>holemenu</i> to <b>OleSetMenuDescriptor</b>.

If both the <i>lpFrame</i> and <i>lpActiveObj</i> parameters are non-<b>NULL</b>, OLE installs the context-sensitive help F1 message filter for the application. Otherwise, the application must supply its own message filter.





## -see-also




<a href="https://msdn.microsoft.com/b077c256-1109-494c-95c2-2d33bccbe47b">IOleInPlaceActiveObject</a>



<a href="https://msdn.microsoft.com/dc26a399-846d-4d15-b406-752350e528c2">IOleInPlaceFrame::SetMenu</a>



<a href="https://msdn.microsoft.com/b4a6b3f1-aee9-4b68-8ffe-24bd497db0a0">OleCreateMenuDescriptor</a>
 

 

