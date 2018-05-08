---
UID: NF:mfidl.IMFRateControl.GetRate
title: IMFRateControl::GetRate
author: windows-driver-content
description: Gets the current playback rate.
old-location: mf\imfratecontrol_getrate.htm
old-project: medfound
ms.assetid: fb970d06-0f82-4e35-8e03-68044c7f12cd
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetRate, GetRate method [Media Foundation], GetRate method [Media Foundation],IMFRateControl interface, IMFRateControl interface [Media Foundation],GetRate method, IMFRateControl.GetRate, IMFRateControl::GetRate, fb970d06-0f82-4e35-8e03-68044c7f12cd, mf.imfratecontrol_getrate, mfidl/IMFRateControl::GetRate
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IMFRateControl.GetRate
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFRateControl::GetRate


## -description



Gets the current playback rate.




## -parameters




### -param pfThin [in, out]

Receives the value <b>TRUE</b> if the stream is currently being thinned. If the object does not support thinning, this parameter always receives the value <b>FALSE</b>. This parameter can be <b>NULL</b>. For more information, see <a href="https://msdn.microsoft.com/509b2cc8-6017-41a9-ae80-9af21dce9367">About Rate Control</a>.


### -param pflRate [in, out]

Receives the current playback rate.


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




<a href="https://msdn.microsoft.com/7f2b64e1-1062-4f77-b8e0-62b6d962ae8b">How to Determine Supported Rates</a>



<a href="https://msdn.microsoft.com/54303c32-b260-4364-9130-a592694f2816">IMFRateControl</a>
 

 

