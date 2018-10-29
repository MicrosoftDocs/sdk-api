---
UID: NF:wmcodecdsp.ITocEntryList.AddEntryByIndex
title: ITocEntryList::AddEntryByIndex
author: windows-sdk-content
description: The AddEntryByIndex method adds an individual entry to the list and associates a caller-supplied index with the entry.
old-location: mf\itocentrylist_addentrybyindex.htm
tech.root: medfound
ms.assetid: c8146c0f-ac91-42c7-9368-dd2db6079d3d
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AddEntryByIndex, AddEntryByIndex method [Media Foundation], AddEntryByIndex method [Media Foundation],ITocEntryList interface, ITocEntryList interface [Media Foundation],AddEntryByIndex method, ITocEntryList.AddEntryByIndex, ITocEntryList::AddEntryByIndex, codecapi.itocentrylist_addentrybyindex, mf.itocentrylist_addentrybyindex, wmcodecdsp/ITocEntryList::AddEntryByIndex
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
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmvdspa.dll
api_name:
 - ITocEntryList.AddEntryByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITocEntryList::AddEntryByIndex


## -description


The <b>AddEntryByIndex</b> method adds an individual entry to the list and associates a caller-supplied index with the entry.


## -parameters




### -param dwEntryIndex [in]

The index of the entry to be added.


### -param pEntry [in]

Pointer to an <a href="https://msdn.microsoft.com/82a1a390-50b1-4699-9baa-60cea322ce7c">ITocEntry</a> interface that represents the entry to be added.


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




<a href="https://msdn.microsoft.com/cf2171c9-67ce-4acb-97cc-af17203e815b">GetEntryByIndex</a>



<a href="https://msdn.microsoft.com/98052f26-7956-4973-ab86-428e7a355937">ITocEntryList</a>
 

 

