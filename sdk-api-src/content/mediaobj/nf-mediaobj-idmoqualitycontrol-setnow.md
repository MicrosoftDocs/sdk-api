---
UID: NF:mediaobj.IDMOQualityControl.SetNow
title: IDMOQualityControl::SetNow method
author: windows-driver-content
description: The SetNow method specifies the earliest time stamp that the DMO will deliver.
old-location: dshow\idmoqualitycontrol_setnow.htm
old-project: DirectShow
ms.assetid: 36efee4f-0a06-421f-bc37-688a6499bda7
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IDMOQualityControl, IDMOQualityControl interface [DirectShow], SetNow method, IDMOQualityControl::SetNow, IDMOQualityControlSetNow, SetNow method [DirectShow], SetNow method [DirectShow], IDMOQualityControl interface, SetNow,IDMOQualityControl.SetNow, dshow.idmoqualitycontrol_setnow, mediaobj/IDMOQualityControl::SetNow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mediaobj.h
req.include-header: Dmo.h
req.target-type: Windows
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dmoguids.lib
-	Dmoguids.dll
api_name:
-	IDMOQualityControl.SetNow
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDMOQualityControl::SetNow method


## -description



The <code>SetNow</code> method specifies the earliest time stamp that the DMO will deliver.




## -parameters




### -param rtNow [in]

Reference time specifying the earliest time stamp to deliver.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



If quality control is enabled, the DMO discards any samples whose time stamp is less than <i>rtNow</i>. Samples whose time stamp is <i>rtNow</i> or later are processed as efficiently as possible. Depending on the implementation, the DMO might drop some samples to keep pace.

If quality control is disabled, this method has no immediate effect. However, the DMO stores the specified reference time. It uses this value if quality control is enabled at a later time. To enable quality control, call the <a href="https://msdn.microsoft.com/d22a7a23-6623-4a98-9a0c-5195b29781f9">IDMOQualityControl::SetStatus</a> method.

If incoming samples are not time-stamped, the DMO never performs quality control. The application sets the time stamp in the <a href="https://msdn.microsoft.com/f52e9586-f65d-418f-8c1a-c97c0a81d253">IMediaObject::ProcessInput</a> method.




## -see-also




<a href="https://msdn.microsoft.com/c23211f2-d4ba-45ff-b443-3425c3a3e72f">IDMOQualityControl Interface</a>
 

 

