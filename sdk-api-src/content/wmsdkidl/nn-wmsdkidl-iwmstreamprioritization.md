---
UID: NN:wmsdkidl.IWMStreamPrioritization
title: IWMStreamPrioritization (wmsdkidl.h)
description: The IWMStreamPrioritization interface provides methods to set and read priority records for a file.Stream prioritization allows content creators to specify the priority of the streams in an ASF file.helpviewer_keywords: ["IWMStreamPrioritization","IWMStreamPrioritization interface [windows Media Format]","IWMStreamPrioritization interface [windows Media Format]","described","IWMStreamPrioritizationInterface","wmformat.iwmstreamprioritization","wmsdkidl/IWMStreamPrioritization"]
old-location: wmformat\iwmstreamprioritization.htm
tech.root: wmformat
ms.assetid: ef8ae275-c36a-492c-b57c-d640044ede93
ms.date: 12/05/2018
ms.keywords: IWMStreamPrioritization, IWMStreamPrioritization interface [windows Media Format], IWMStreamPrioritization interface [windows Media Format],described, IWMStreamPrioritizationInterface, wmformat.iwmstreamprioritization, wmsdkidl/IWMStreamPrioritization
f1_keywords:
- wmsdkidl/IWMStreamPrioritization
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmsdkidl.h
api_name:
- IWMStreamPrioritization
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMStreamPrioritization interface


## -description



The <b>IWMStreamPrioritization</b> interface provides methods to set and read priority records for a file.

Stream prioritization allows content creators to specify the priority of the streams in an ASF file. The streams assigned the lowest priority will be dropped first in the case of insufficient bit rate during playback.

Only one stream prioritization object can exist for a profile. You can check to see if one is present with a call to <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization">IWMProfile3::GetStreamPrioritization</a>, which will retrieve a pointer to one if it exists.

You can create a new stream prioritization object with a call to <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization">IWMProfile3::CreateNewStreamPrioritization</a>. You will then receive a pointer to <b>IWMStreamPrioritization</b> for the new object. This will erase the existing stream prioritization, if there is one.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMStreamPrioritization</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMStreamPrioritization</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamprioritization-getpriorityrecords">GetPriorityRecords</a>
</td>
<td align="left" width="63%">
Retrieves the list of streams and their priorities from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamprioritization-setpriorityrecords">SetPriorityRecords</a>
</td>
<td align="left" width="63%">
Set the list of streams and their priorities for the profile.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/stream-prioritization-object">Stream Prioritization Object</a>
 

 

