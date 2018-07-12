---
UID: NF:mediaobj.IDMOQualityControl.SetStatus
title: IDMOQualityControl::SetStatus
author: windows-sdk-content
description: The SetStatus method enables or disables quality control.
old-location: dshow\idmoqualitycontrol_setstatus.htm
old-project: DirectShow
ms.assetid: d22a7a23-6623-4a98-9a0c-5195b29781f9
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IDMOQualityControl interface [DirectShow],SetStatus method, IDMOQualityControl.SetStatus, IDMOQualityControl::SetStatus, IDMOQualityControlSetStatus, SetStatus, SetStatus method [DirectShow], SetStatus method [DirectShow],IDMOQualityControl interface, dshow.idmoqualitycontrol_setstatus, mediaobj/IDMOQualityControl::SetStatus
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
 - IDMOQualityControl.SetStatus
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDMOQualityControl::SetStatus


## -description



The <code>SetStatus</code> method enables or disables quality control.




## -parameters




### -param dwFlags [in]

Value that specifies whether to enable or disable quality control. Use DMO_QUALITY_STATUS_ENABLED to enable quality control, or zero to disable quality control.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument

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



With quality control enabled, the DMO attempts to deliver samples on time. It can skip late samples if necessary. With quality control disabled, the DMO delivers every sample. If you enable quality control, call the <a href="https://msdn.microsoft.com/36efee4f-0a06-421f-bc37-688a6499bda7">IDMOQualityControl::SetNow</a> method to specify the earliest time stamp that the DMO should process. Otherwise, the call to <code>SetStatus</code> succeeds but the DMO does not perform quality control.

By default, quality control is disabled.




## -see-also




<a href="https://msdn.microsoft.com/c23211f2-d4ba-45ff-b443-3425c3a3e72f">IDMOQualityControl Interface</a>
 

 

