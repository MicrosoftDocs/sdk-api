---
UID: NF:mfidl.IMFContentEnabler.AutomaticEnable
title: IMFContentEnabler::AutomaticEnable
author: windows-sdk-content
description: Performs a content enabling action without any user interaction.
old-location: mf\imfcontentenabler_automaticenable.htm
tech.root: medfound
ms.assetid: 7be4c32f-d116-4a08-857f-1a59b5ccfb12
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: 7be4c32f-d116-4a08-857f-1a59b5ccfb12, AutomaticEnable, AutomaticEnable method [Media Foundation], AutomaticEnable method [Media Foundation],IMFContentEnabler interface, IMFContentEnabler interface [Media Foundation],AutomaticEnable method, IMFContentEnabler.AutomaticEnable, IMFContentEnabler::AutomaticEnable, mf.imfcontentenabler_automaticenable, mfidl/IMFContentEnabler::AutomaticEnable
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMFContentEnabler.AutomaticEnable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFContentEnabler::AutomaticEnable


## -description



Performs a content enabling action without any user interaction.




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



This method is asynchronous. When the operation is complete, the content enabler sends an <a href="https://msdn.microsoft.com/5162800c-9c55-40de-be66-a98765324f76">MEEnablerCompleted</a> event. While the operation is in progress, the content enabler might send <a href="https://msdn.microsoft.com/ec14ba9b-cfb6-4e32-870e-2436e11c308b">MEEnablerProgress</a> events.

To find out whether the content enabler supports this method, call <a href="https://msdn.microsoft.com/144470ce-2849-4464-8596-fac216529145">IMFContentEnabler::IsAutomaticSupported</a>.




## -see-also




<a href="https://msdn.microsoft.com/85d98f49-8af2-42ce-9b36-a025aee93f73">How to Play Protected Media Files</a>



<a href="https://msdn.microsoft.com/45d02bd0-1104-47ec-8559-8cc51590fc62">IMFContentEnabler</a>
 

 

