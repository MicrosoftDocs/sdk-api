---
UID: NN:wmsdkidl.IWMStreamPrioritization
title: IWMStreamPrioritization
author: windows-sdk-content
description: The IWMStreamPrioritization interface provides methods to set and read priority records for a file.Stream prioritization allows content creators to specify the priority of the streams in an ASF file.
old-location: wmformat\iwmstreamprioritization.htm
old-project: wmformat
ms.assetid: ef8ae275-c36a-492c-b57c-d640044ede93
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMStreamPrioritization, IWMStreamPrioritization interface [windows Media Format], IWMStreamPrioritization interface [windows Media Format],described, IWMStreamPrioritizationInterface, wmformat.iwmstreamprioritization, wmsdkidl/IWMStreamPrioritization
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
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
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMStreamPrioritization
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMStreamPrioritization interface


## -description



The <b>IWMStreamPrioritization</b> interface provides methods to set and read priority records for a file.

Stream prioritization allows content creators to specify the priority of the streams in an ASF file. The streams assigned the lowest priority will be dropped first in the case of insufficient bit rate during playback.

Only one stream prioritization object can exist for a profile. You can check to see if one is present with a call to <a href="https://msdn.microsoft.com/09545c1e-8090-4526-9faf-6cb2cb369208">IWMProfile3::GetStreamPrioritization</a>, which will retrieve a pointer to one if it exists.

You can create a new stream prioritization object with a call to <a href="https://msdn.microsoft.com/801a66fa-b72d-4282-953e-216fb9a56cd7">IWMProfile3::CreateNewStreamPrioritization</a>. You will then receive a pointer to <b>IWMStreamPrioritization</b> for the new object. This will erase the existing stream prioritization, if there is one.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMStreamPrioritization</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMStreamPrioritization</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMStreamPrioritization</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50b105c7-1e4f-435c-8bb6-643ea4d065bb">GetPriorityRecords</a>
</td>
<td align="left" width="63%">
Retrieves the list of streams and their priorities from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bd42132-b391-4941-87db-5ce2254e19cf">SetPriorityRecords</a>
</td>
<td align="left" width="63%">
Set the list of streams and their priorities for the profile.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3 Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/cb0345ce-6847-435b-8cbb-f8b93856af9f">Stream Prioritization Object</a>
 

 

