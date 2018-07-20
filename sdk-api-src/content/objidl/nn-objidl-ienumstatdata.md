---
UID: NN:objidl.IEnumSTATDATA
title: IEnumSTATDATA
author: windows-sdk-content
description: Enumerates the advisory connection information for a data object.
old-location: com\ienumstatdata.htm
old-project: com
ms.assetid: 8e2f6655-4a09-4868-a909-18999104b3ff
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IEnumSTATDATA, IEnumSTATDATA interface [COM], IEnumSTATDATA interface [COM],described, _ole_ienumstatdata, com.ienumstatdata, objidl/IEnumSTATDATA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IEnumSTATDATA
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IEnumSTATDATA interface


## -description


Enumerates the advisory connection information for a data object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSTATDATA</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IEnumSTATDATA</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSTATDATA</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0863d013-6f55-40ce-92d2-68bb0455a911">IDataAdviseHolder::EnumAdvise</a>



<a href="https://msdn.microsoft.com/319637fd-d9b5-4da0-ac92-4c52fa9f5231">IDataObject::EnumDAdvise</a>



<a href="https://msdn.microsoft.com/80a9ccd8-f89a-40c4-8b99-38536409cf26">IOleAdviseHolder::EnumAdvise</a>



<a href="https://msdn.microsoft.com/a8d99926-8fb9-4624-8025-483101cb9311">IOleCache::EnumCache</a>
 

 

