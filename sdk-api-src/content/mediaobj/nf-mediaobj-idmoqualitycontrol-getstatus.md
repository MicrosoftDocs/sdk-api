---
UID: NF:mediaobj.IDMOQualityControl.GetStatus
title: IDMOQualityControl::GetStatus
author: windows-sdk-content
description: The GetStatus method determines whether quality control is active.
old-location: dshow\idmoqualitycontrol_getstatus.htm
old-project: DirectShow
ms.assetid: 5c45874f-5546-40cc-a113-bea92bd9784b
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetStatus, GetStatus method [DirectShow], GetStatus method [DirectShow],IDMOQualityControl interface, IDMOQualityControl interface [DirectShow],GetStatus method, IDMOQualityControl.GetStatus, IDMOQualityControl::GetStatus, IDMOQualityControlGetStatus, dshow.idmoqualitycontrol_getstatus, mediaobj/IDMOQualityControl::GetStatus
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IDMOQualityControl.GetStatus
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDMOQualityControl::GetStatus


## -description



The <code>GetStatus</code> method determines whether quality control is active.




## -parameters




### -param pdwFlags [out]

Pointer to a variable that receives the quality control status. If quality control is disabled, the value is zero. If quality control is enabled, the value is DMO_QUALITY_STATUS_ENABLED.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer value

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
 




## -see-also




<a href="https://msdn.microsoft.com/c23211f2-d4ba-45ff-b443-3425c3a3e72f">IDMOQualityControl Interface</a>
 

 

