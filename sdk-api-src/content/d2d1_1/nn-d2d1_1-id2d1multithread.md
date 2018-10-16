---
UID: NN:d2d1_1.ID2D1Multithread
title: ID2D1Multithread
author: windows-sdk-content
description: A locking mechanism from a Direct2D factory that Direct2D uses to control exclusive resource access in an app that is uses multiple threads.
old-location: direct2d\id2d1multithread.htm
tech.root: direct2d
ms.assetid: 885E7580-6BF0-4A44-9493-6D4FFCB5577B
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ID2D1Multithread, ID2D1Multithread interface [Direct2D], ID2D1Multithread interface [Direct2D],described, d2d1_1/ID2D1Multithread, direct2d.id2d1multithread
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Multithread
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Multithread interface


## -description


A  locking mechanism from a <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> factory that Direct2D 
          uses to control exclusive resource access in an app that is uses multiple threads.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Multithread</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID2D1Multithread</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Multithread</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5578DAC4-90C6-4E6D-B38B-D5AC301A8DB2">Enter</a>
</td>
<td align="left" width="63%">
Enters the Direct2D API critical section, if it exists. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C805B8C1-942B-4E56-97F2-756B0DD800A2">GetMultithreadProtected</a>
</td>
<td align="left" width="63%">
Returns whether the Direct2D factory was created with the <a href="https://msdn.microsoft.com/428053d3-7ea0-4b01-9924-4a31d8e018fb">D2D1_FACTORY_TYPE_MULTI_THREADED</a> flag.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C5A7DB35-3AB8-4BB9-A75E-6DA1480738C2">Leave</a>
</td>
<td align="left" width="63%">
Leaves the Direct2D API critical section, if it exists.

</td>
</tr>
</table> 


## -remarks



You can get an <b>ID2D1Multithread</b> object by querying for it from an <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a> 
        object.
      

You should use this lock while doing any operation on a Direct3D/DXGI surface. <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> will wait on any call until you 
        leave the critical section.
      

<div class="alert"><b>Note</b>  Normal rendering is guarded automatically by an internal <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> lock.
        </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>
 

 

