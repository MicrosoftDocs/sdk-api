---
UID: NF:mpeg2data.ISectionList.GetNumberOfSections
title: ISectionList::GetNumberOfSections (mpeg2data.h)
author: windows-sdk-content
description: The GetNumberOfSections method returns the number of MPEG-2 sections that were received.
old-location: mstv\isectionlist_getnumberofsections.htm
tech.root: mstv
ms.assetid: 4b9e3383-7b84-4c4e-87cf-8e3a37d3b81b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetNumberOfSections, GetNumberOfSections method [Microsoft TV Technologies], GetNumberOfSections method [Microsoft TV Technologies],ISectionList interface, ISectionList interface [Microsoft TV Technologies],GetNumberOfSections method, ISectionList.GetNumberOfSections, ISectionList::GetNumberOfSections, ISectionListGetNumberOfSections, mpeg2data/ISectionList::GetNumberOfSections, mstv.isectionlist_getnumberofsections
ms.topic: method
req.header: mpeg2data.h
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
 - Mpeg2data.h
api_name:
 - ISectionList.GetNumberOfSections
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISectionList::GetNumberOfSections


## -description



The <b>GetNumberOfSections</b> method returns the number of MPEG-2 sections that were received.




## -parameters




### -param pCount [out]

Receives the number of sections.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The request has not completed yet.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
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
 




## -see-also




<a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList Interface</a>
 

 

