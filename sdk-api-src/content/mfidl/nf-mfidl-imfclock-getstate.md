---
UID: NF:mfidl.IMFClock.GetState
title: IMFClock::GetState
author: windows-sdk-content
description: Retrieves the current state of the clock.
old-location: mf\imfclock_getstate.htm
old-project: medfound
ms.assetid: 8e2dda03-f589-4572-b715-2be7b29a6ace
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 8e2dda03-f589-4572-b715-2be7b29a6ace, GetState, GetState method [Media Foundation], GetState method [Media Foundation],IMFClock interface, IMFClock interface [Media Foundation],GetState method, IMFClock.GetState, IMFClock::GetState, mf.imfclock_getstate, mfidl/IMFClock::GetState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
-	IMFClock.GetState
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFClock::GetState


## -description



Retrieves the current state of the clock.




## -parameters




### -param dwReserved [in]

Reserved, must be zero.


### -param peClockState [out]

Receives the clock state, as a member of the <a href="https://msdn.microsoft.com/90e04807-c3be-4f38-a508-9dfe62700869">MFCLOCK_STATE</a> enumeration.


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
 




## -see-also




<a href="https://msdn.microsoft.com/3a60bfec-8511-4a84-a833-e0c73c593970">IMFClock</a>
 

 

