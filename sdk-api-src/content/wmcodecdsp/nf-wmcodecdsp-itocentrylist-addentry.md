---
UID: NF:wmcodecdsp.ITocEntryList.AddEntry
title: ITocEntryList::AddEntry
author: windows-sdk-content
description: The AddEntry method adds an individual entry to the list and assigns an index to the entry.
old-location: mf\itocentrylist_addentry.htm
tech.root: medfound
ms.assetid: 4ac41f10-4bb5-4d50-9f7b-7c8710476162
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AddEntry, AddEntry method [Media Foundation], AddEntry method [Media Foundation],ITocEntryList interface, ITocEntryList interface [Media Foundation],AddEntry method, ITocEntryList.AddEntry, ITocEntryList::AddEntry, codecapi.itocentrylist_addentry, mf.itocentrylist_addentry, wmcodecdsp/ITocEntryList::AddEntry
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
 - ITocEntryList.AddEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITocEntryList::AddEntry


## -description


The <b>AddEntry</b> method adds an individual entry to the list and assigns an index to the entry.


## -parameters




### -param pEntry [in]

Pointer to an <a href="https://msdn.microsoft.com/82a1a390-50b1-4699-9baa-60cea322ce7c">ITocEntry</a> interface that represents the entry to be added.


### -param pdwEntryIndex [out]

Pointer to a <b>DWORD</b> that receives the index of the added entry.


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
 

 

