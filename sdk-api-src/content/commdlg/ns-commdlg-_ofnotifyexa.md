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

# _OFNOTIFYEXA structure


## -description


Contains information about a <a href="https://msdn.microsoft.com/0972a78d-e058-4bac-85bd-fbd4c3885552">CDN_INCLUDEITEM</a> notification message. 


## -struct-fields




### -field hdr

Type: <b><a href="controls._win32_NMHDR_str">NMHDR</a></b>

The <b>code</b> member of this structure identifies the notification message being sent. 


### -field lpOFN

Type: <b>LPOPENFILENAME</b>

A pointer to an <a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a> structure containing the values specified when the <b>Open</b> or <b>Save As</b> dialog box was created. 


### -field psf

Type: <b>LPVOID</b>

A pointer to the  interface for the folder or shell name-space extension whose items are being enumerated. 


### -field pidl

Type: <b>LPVOID</b>

A pointer to an item identifier list that identifies an item in the container identified by the <b>psf</b> member. The item identifier is relative to the <b>psf</b> container. 


## -see-also




<a href="https://msdn.microsoft.com/0972a78d-e058-4bac-85bd-fbd4c3885552">CDN_INCLUDEITEM</a>



<a href="https://msdn.microsoft.com/28573019-f0bd-4a8e-a1a1-48559f658a81">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3d3a7878-1ccc-4832-9351-8f9cf6c7a601">OFNHookProc</a>



<a href="https://msdn.microsoft.com/8d13e45d-e39c-40b0-9cf4-7ddcb5bab1f8">OFNOTIFY</a>



<a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a>



<b>Reference</b>
 

 

