---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# tagOIFI structure


## -description


Contains information about the accelerators supported by a container during an in-place session. The structure is used in the <a href="https://msdn.microsoft.com/f6cf62b3-5a64-49aa-b0bd-56744ecee313">IOleInPlaceSite::GetWindowContext</a> method and the <a href="https://msdn.microsoft.com/c590efef-7f03-4ae6-a35f-eff2fc4da3d9">OleTranslateAccelerator</a> function.


## -struct-fields




### -field cb

The size of this structure, in bytes. The object server must specify sizeof(<b>OLEINPLACEFRAMEINFO</b>) in the structure it passes to <a href="https://msdn.microsoft.com/f6cf62b3-5a64-49aa-b0bd-56744ecee313">IOleInPlaceSite::GetWindowContext</a>. The container can then use this size to determine the structure's version.


### -field fMDIApp

Indicates whether the container is an MDI application.


### -field hwndFrame

A handle to the container's top-level frame window.


### -field haccel

A handle to the accelerator table that the container wants to use during an in-place editing session.


### -field cAccelEntries

The number of accelerators in <b>haccel</b>.



## -remarks



When an object is being in-place activated, its server calls the container's <a href="https://msdn.microsoft.com/f6cf62b3-5a64-49aa-b0bd-56744ecee313">IOleInPlaceSite::GetWindowContext</a> method, which fills in an <b>OLEINPLACEFRAMEINFO</b> structure. During an in-place session, the message loop of an EXE server passes a pointer to the <b>OLEINPLACEFRAMEINFO</b> structure to <a href="https://msdn.microsoft.com/c590efef-7f03-4ae6-a35f-eff2fc4da3d9">OleTranslateAccelerator</a>. OLE uses the information in this structure to determine whether a message maps to one of the container's accelerators.




## -see-also




<a href="https://msdn.microsoft.com/f6cf62b3-5a64-49aa-b0bd-56744ecee313">IOleInPlaceSite::GetWindowContext</a>



<a href="https://msdn.microsoft.com/c590efef-7f03-4ae6-a35f-eff2fc4da3d9">OleTranslateAccelerator</a>
 

 

