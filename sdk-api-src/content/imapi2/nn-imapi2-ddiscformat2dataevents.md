---
UID: NN:imapi2.DDiscFormat2DataEvents
title: DDiscFormat2DataEvents (imapi2.h)
author: windows-sdk-content
description: Implement this interface to receive notifications of the current write operation.
old-location: imapi\ddiscformat2dataevents.htm
tech.root: imapi
ms.assetid: f9f1d976-9ec9-40a5-92b6-d00a7e15d0aa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DDiscFormat2DataEvents, DDiscFormat2DataEvents interface [IMAPI], DDiscFormat2DataEvents interface [IMAPI],described, imapi.ddiscformat2dataevents, imapi2/DDiscFormat2DataEvents
ms.topic: interface
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - DDiscFormat2DataEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DDiscFormat2DataEvents interface


## -description


Implement this interface to receive notifications of the current write operation. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">DDiscFormat2DataEvents</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>DDiscFormat2DataEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>DDiscFormat2DataEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-ddiscformat2dataevents-update">Update</a>
</td>
<td align="left" width="63%">
Implement this method to receive progress notification of the current write operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>
 

 

