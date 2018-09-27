---
UID: NF:mfidl.IMFContentEnabler.IsAutomaticSupported
title: IMFContentEnabler::IsAutomaticSupported
author: windows-sdk-content
description: Queries whether the content enabler can perform all of its actions automatically.
old-location: mf\imfcontentenabler_isautomaticsupported.htm
tech.root: medfound
ms.assetid: 144470ce-2849-4464-8596-fac216529145
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 144470ce-2849-4464-8596-fac216529145, IMFContentEnabler interface [Media Foundation],IsAutomaticSupported method, IMFContentEnabler.IsAutomaticSupported, IMFContentEnabler::IsAutomaticSupported, IsAutomaticSupported, IsAutomaticSupported method [Media Foundation], IsAutomaticSupported method [Media Foundation],IMFContentEnabler interface, mf.imfcontentenabler_isautomaticsupported, mfidl/IMFContentEnabler::IsAutomaticSupported
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
 - IMFContentEnabler.IsAutomaticSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFContentEnabler::IsAutomaticSupported


## -description



Queries whether the content enabler can perform all of its actions automatically.




## -parameters




### -param pfAutomatic [out]

Receives a Boolean value. If <b>TRUE</b>, the content enabler can perform the enabing action automatically.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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



If this method returns <b>TRUE</b> in the <i>pfAutomatic</i> parameter, call the <a href="https://msdn.microsoft.com/7be4c32f-d116-4a08-857f-1a59b5ccfb12">IMFContentEnabler::AutomaticEnable</a> method to perform the enabling action.

If this method returns <b>FALSE</b> in the <i>pfAutomatic</i> parameter, the application must use manual enabling. To do so, call <a href="https://msdn.microsoft.com/1a44216d-36e5-4b5c-9585-5297d5e429f9">IMFContentEnabler::GetEnableURL</a> and <a href="https://msdn.microsoft.com/d1859037-7a33-4943-8ca9-6782fc8b0b92">IMFContentEnabler::GetEnableData</a> to get the URL and data needed for manual enabling.




## -see-also




<a href="https://msdn.microsoft.com/85d98f49-8af2-42ce-9b36-a025aee93f73">How to Play Protected Media Files</a>



<a href="https://msdn.microsoft.com/45d02bd0-1104-47ec-8559-8cc51590fc62">IMFContentEnabler</a>
 

 

