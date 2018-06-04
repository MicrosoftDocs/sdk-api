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

# GdiplusAbort structure


## -description


The <b>GdiplusAbort</b> structure provides a mechanism that allows Windows GDI+ to call an application-defined <b>Abort</b> method periodically during time-consuming rendering operations.


## -struct-fields


## -remarks



The <b>GdiplusAbort</b> structure has only one method, a virtual method named <b>Abort</b>. The <b>GdiplusAbort</b> structure has no data members.

To create a callback method, follow these steps.

<ol>
<li>
Create a structure that descends from <b>GdiplusAbort</b>, and implement the following method.

<code>HRESULT __stdcall Abort(void)</code>

</li>
<li>Create data members to hold any data that will be needed by the <b>Abort</b> method.</li>
<li>Pass the address of the <b>GdiplusAbort</b> descendant to the <a href="https://msdn.microsoft.com/2df54a2c-cb7b-4d65-a27d-7342e00ed71b">Image::SetAbort</a> method.</li>
</ol>
During certain time-consuming rendering operations (for example, a call to the <a href="https://msdn.microsoft.com/c9577988-e52f-4f71-ab1b-51bb5368812e">Graphics::DrawImage</a> method), GDI+ calls the <b>Abort</b> method periodically. For some operations the callback is every 250 milliseconds; for other operations the callback is not based on a timer. If the <b>Abort</b> method returns S_OK, GDI+ continues the rendering operation. If the <b>Abort</b> method returns E_ABORT, GDI+ aborts the rendering operation.



