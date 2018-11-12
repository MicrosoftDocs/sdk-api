---
UID: NF:mfapi.MFCreateEventQueue
title: MFCreateEventQueue function
author: windows-sdk-content
description: Creates an event queue.
old-location: mf\mfcreateeventqueue.htm
tech.root: medfound
ms.assetid: 214cea99-37cf-4571-aa00-7b3e220a6b84
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 214cea99-37cf-4571-aa00-7b3e220a6b84, MFCreateEventQueue, MFCreateEventQueue function [Media Foundation], mf.mfcreateeventqueue, mfapi/MFCreateEventQueue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateEventQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateEventQueue function


## -description



Creates an event queue.




## -parameters




### -param ppMediaEventQueue

Receives a pointer to the <a href="https://msdn.microsoft.com/e1698caa-db70-436d-af6a-64c6e7247590">IMFMediaEventQueue</a> interface of the event queue. The caller must release the interface.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



This function creates a helper object that you can use to implement the <a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a> interface.

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/2e003ad4-9fcb-4834-a335-e4969ffd3a00">Media Event Generators</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

