---
UID: NF:mfidl.IMFContentEnabler.MonitorEnable
title: IMFContentEnabler::MonitorEnable (mfidl.h)
author: windows-sdk-content
description: Requests notification when the enabling action is completed.
old-location: mf\imfcontentenabler_monitorenable.htm
tech.root: medfound
ms.assetid: 78fc4a17-f58c-4654-b37e-6b988848ff0d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 78fc4a17-f58c-4654-b37e-6b988848ff0d, IMFContentEnabler interface [Media Foundation],MonitorEnable method, IMFContentEnabler.MonitorEnable, IMFContentEnabler::MonitorEnable, MonitorEnable, MonitorEnable method [Media Foundation], MonitorEnable method [Media Foundation],IMFContentEnabler interface, mf.imfcontentenabler_monitorenable, mfidl/IMFContentEnabler::MonitorEnable
ms.topic: method
req.header: mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFContentEnabler.MonitorEnable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFContentEnabler::MonitorEnable


## -description



Requests notification when the enabling action is completed.




## -parameters






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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded and no action was required.

</td>
</tr>
</table>
 




## -remarks



If you use a manual enabling action, call this method to be notified when the operation completes. If this method returns S_OK, the content enabler will send an <a href="https://msdn.microsoft.com/5162800c-9c55-40de-be66-a98765324f76">MEEnablerCompleted</a> event when the operation is completed. If the application cancels the operatation before completing it, call <a href="https://msdn.microsoft.com/e273b702-1f42-4aeb-9259-778d3f206682">IMFContentEnabler::Cancel</a>.

You do not have to call <b>MonitorEnable</b> when you use automatic enabling by calling <a href="https://msdn.microsoft.com/7be4c32f-d116-4a08-857f-1a59b5ccfb12">IMFContentEnabler::AutomaticEnable</a>.




## -see-also




<a href="https://msdn.microsoft.com/85d98f49-8af2-42ce-9b36-a025aee93f73">How to Play Protected Media Files</a>



<a href="https://msdn.microsoft.com/45d02bd0-1104-47ec-8559-8cc51590fc62">IMFContentEnabler</a>
 

 

