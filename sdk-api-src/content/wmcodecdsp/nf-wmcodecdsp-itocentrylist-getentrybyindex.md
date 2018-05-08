---
UID: NF:wmcodecdsp.ITocEntryList.GetEntryByIndex
title: ITocEntryList::GetEntryByIndex
author: windows-driver-content
description: The GetEntryByIndex method retrieves an entry, specified by an index, from the list.
old-location: mf\itocentrylist_getentrybyindex.htm
old-project: medfound
ms.assetid: cf2171c9-67ce-4acb-97cc-af17203e815b
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetEntryByIndex, GetEntryByIndex method [Media Foundation], GetEntryByIndex method [Media Foundation],ITocEntryList interface, ITocEntryList interface [Media Foundation],GetEntryByIndex method, ITocEntryList.GetEntryByIndex, ITocEntryList::GetEntryByIndex, codecapi.itocentrylist_getentrybyindex, mf.itocentrylist_getentrybyindex, wmcodecdsp/ITocEntryList::GetEntryByIndex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFVideoDSPMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmvdspa.dll
api_name:
-	ITocEntryList.GetEntryByIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ITocEntryList::GetEntryByIndex


## -description


The <b>GetEntryByIndex</b> method retrieves an entry, specified by an index, from the list.


## -parameters




### -param dwEntryIndex [in]

The index of the entry to retrieve.


### -param ppEntry [out]

Pointer to a variable that receives a pointer to an <a href="https://msdn.microsoft.com/82a1a390-50b1-4699-9baa-60cea322ce7c">ITocEntry</a> interface that represents the entry.


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
 




## -see-also




<a href="https://msdn.microsoft.com/c8146c0f-ac91-42c7-9368-dd2db6079d3d">AddEntryByIndex</a>



<a href="https://msdn.microsoft.com/98052f26-7956-4973-ab86-428e7a355937">ITocEntryList</a>
 

 

