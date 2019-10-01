---
UID: NN:winsync.IEnumSingleItemExceptions
title: IEnumSingleItemExceptions (winsync.h)
author: windows-sdk-content
description: Enumerates single-item exceptions that are stored in a knowledge object.
old-location: winsync\ienumsingleitemexceptions.htm
tech.root: winsync
ms.assetid: fed8a258-bc23-454b-9d8a-e3873481b33b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumSingleItemExceptions, IEnumSingleItemExceptions interface [Windows Sync], IEnumSingleItemExceptions interface [Windows Sync],described, winsync.ienumsingleitemexceptions, winsync/IEnumSingleItemExceptions
ms.topic: interface
f1_keywords: 
 - "winsync/IEnumSingleItemExceptions"
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - winsync.h
api_name:
 - IEnumSingleItemExceptions
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSingleItemExceptions interface


## -description


Enumerates single-item exceptions that are stored in a knowledge object.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSingleItemExceptions</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSingleItemExceptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSingleItemExceptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumsingleitemexceptions-clone">Clone</a>
</td>
<td align="left" width="63%">
Clones the enumerator and returns a new enumerator that is in the same state as the current one.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumsingleitemexceptions-next">Next</a>
</td>
<td align="left" width="63%">
Returns the next elements in the single-item exception set, if they are available.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumsingleitemexceptions-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator to the beginning of the single-item exception set.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumsingleitemexceptions-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of single item exceptions.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

