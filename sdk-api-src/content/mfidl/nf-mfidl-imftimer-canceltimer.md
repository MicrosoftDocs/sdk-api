---
UID: NF:mfidl.IMFTimer.CancelTimer
title: IMFTimer::CancelTimer method
author: windows-driver-content
description: Cancels a timer that was set using the IMFTimer::SetTimer method.
old-location: mf\imftimer_canceltimer.htm
old-project: medfound
ms.assetid: 3fa65809-1652-4903-92ad-1034bcdf0743
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: 3fa65809-1652-4903-92ad-1034bcdf0743, CancelTimer method [Media Foundation], CancelTimer method [Media Foundation], IMFTimer interface, CancelTimer,IMFTimer.CancelTimer, IMFTimer, IMFTimer interface [Media Foundation], CancelTimer method, IMFTimer::CancelTimer, mf.imftimer_canceltimer, mfidl/IMFTimer::CancelTimer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFTimer.CancelTimer
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTimer::CancelTimer method


## -description



Cancels a timer that was set using the <a href="https://msdn.microsoft.com/3b583541-6480-490d-883f-376ea95f7a98">IMFTimer::SetTimer</a> method.




## -parameters




### -param punkKey [in]

Pointer to the <b>IUnknown</b> interface that was returned in the <i>ppunkKey</i> parameter of the <a href="https://msdn.microsoft.com/3b583541-6480-490d-883f-376ea95f7a98">SetTimer</a> method.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



Because the timer is dispatched asynchronously, the application's timer callback might get invoked even if this method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/152594df-de3d-4f6f-9277-dba95ab3533a">IMFTimer</a>
 

 

