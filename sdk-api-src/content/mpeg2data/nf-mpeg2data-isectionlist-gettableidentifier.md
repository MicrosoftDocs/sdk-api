---
UID: NF:mpeg2data.ISectionList.GetTableIdentifier
title: ISectionList::GetTableIdentifier
author: windows-sdk-content
description: The GetTableIdentifier method returns the table identifier (TID) of the packets that this object is receiving.
old-location: mstv\isectionlist_gettableidentifier.htm
old-project: mstv
ms.assetid: e0fd82ec-283e-4d6f-aa74-c65f15df651f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetTableIdentifier, GetTableIdentifier method [Microsoft TV Technologies], GetTableIdentifier method [Microsoft TV Technologies],ISectionList interface, ISectionList interface [Microsoft TV Technologies],GetTableIdentifier method, ISectionList.GetTableIdentifier, ISectionList::GetTableIdentifier, ISectionListGetTableIdentifier, mpeg2data/ISectionList::GetTableIdentifier, mstv.isectionlist_gettableidentifier
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mpeg2data.h
req.include-header: 
req.redist: 
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
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2data.h
api_name:
 - ISectionList.GetTableIdentifier
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ISectionList::GetTableIdentifier


## -description



The <b>GetTableIdentifier</b> method returns the table identifier (TID) of the packets that this object is receiving.




## -parameters




### -param pTableId

Receives the TID.


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
 




## -remarks



The TID value is set when the object is first initialized.




## -see-also




<a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList Interface</a>
 

 

