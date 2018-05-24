---
UID: NN:mfidl.IMFTimer
title: IMFTimer
author: windows-driver-content
description: Provides a timer that invokes a callback at a specified time.
old-location: mf\imftimer.htm
old-project: medfound
ms.assetid: 152594df-de3d-4f6f-9277-dba95ab3533a
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: 152594df-de3d-4f6f-9277-dba95ab3533a, IMFTimer, IMFTimer interface [Media Foundation], IMFTimer interface [Media Foundation],described, mf.imftimer, mfidl/IMFTimer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFTimer
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfsensorgroup.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFTimer interface


## -description


Provides a timer that invokes a callback at a specified time.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTimer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTimer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTimer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3fa65809-1652-4903-92ad-1034bcdf0743">CancelTimer</a>
</td>
<td align="left" width="63%">

          Cancels a timer.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b583541-6480-490d-883f-376ea95f7a98">SetTimer</a>
</td>
<td align="left" width="63%">

          Sets a timer that invokes a callback.
        

</td>
</tr>
</table> 


## -remarks



The presentation clock exposes this interface. To get a pointer to the interface, call <b>QueryInterface</b>.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

