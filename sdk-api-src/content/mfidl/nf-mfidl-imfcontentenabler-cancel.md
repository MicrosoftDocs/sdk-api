---
UID: NF:mfidl.IMFContentEnabler.Cancel
title: IMFContentEnabler::Cancel
author: windows-sdk-content
description: Cancels a pending content enabling action.
old-location: mf\imfcontentenabler_cancel.htm
old-project: medfound
ms.assetid: e273b702-1f42-4aeb-9259-778d3f206682
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: Cancel, Cancel method [Media Foundation], Cancel method [Media Foundation],IMFContentEnabler interface, IMFContentEnabler interface [Media Foundation],Cancel method, IMFContentEnabler.Cancel, IMFContentEnabler::Cancel, e273b702-1f42-4aeb-9259-778d3f206682, mf.imfcontentenabler_cancel, mfidl/IMFContentEnabler::Cancel
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFContentEnabler.Cancel
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFContentEnabler::Cancel


## -description



Cancels a pending content enabling action.




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
</table>
 




## -remarks



The content enabler sends an <a href="https://msdn.microsoft.com/5162800c-9c55-40de-be66-a98765324f76">MEEnablerCompleted</a> event with a status code of E_CANCEL.




## -see-also




<a href="https://msdn.microsoft.com/85d98f49-8af2-42ce-9b36-a025aee93f73">How to Play Protected Media Files</a>



<a href="https://msdn.microsoft.com/45d02bd0-1104-47ec-8559-8cc51590fc62">IMFContentEnabler</a>
 

 

