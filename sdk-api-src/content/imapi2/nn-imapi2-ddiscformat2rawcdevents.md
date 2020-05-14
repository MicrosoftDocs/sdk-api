---
UID: NN:imapi2.DDiscFormat2RawCDEvents
title: DDiscFormat2RawCDEvents (imapi2.h)
description: Implement this interface to receive notifications of the current raw-image write operation.helpviewer_keywords: ["DDiscFormat2RawCDEvents","DDiscFormat2RawCDEvents interface [IMAPI]","DDiscFormat2RawCDEvents interface [IMAPI]","described","imapi.ddiscformat2rawcdevents","imapi2/DDiscFormat2RawCDEvents"]
old-location: imapi\ddiscformat2rawcdevents.htm
tech.root: imapi
ms.assetid: 3a06911e-8a50-4e41-874c-478ad05f6488
ms.date: 12/05/2018
ms.keywords: DDiscFormat2RawCDEvents, DDiscFormat2RawCDEvents interface [IMAPI], DDiscFormat2RawCDEvents interface [IMAPI],described, imapi.ddiscformat2rawcdevents, imapi2/DDiscFormat2RawCDEvents
f1_keywords:
- imapi2/DDiscFormat2RawCDEvents
dev_langs:
- c++
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
- DDiscFormat2RawCDEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DDiscFormat2RawCDEvents interface


## -description


Implement this interface to receive notifications of the current raw-image write operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">DDiscFormat2RawCDEvents</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>DDiscFormat2RawCDEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>DDiscFormat2RawCDEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-ddiscformat2rawcdevents-update">Update</a>
</td>
<td align="left" width="63%">
Implement this method to receive progress notification of the current raw-image write operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a>
 

 

