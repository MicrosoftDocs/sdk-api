---
UID: NF:wmcodecdsp.IToc.AddEntryList
title: IToc::AddEntryList
author: windows-sdk-content
description: The AddEntryList method adds an entry list to the table of contents and assigns an index to the entry list.
old-location: mf\itoc_addentrylist.htm
tech.root: medfound
ms.assetid: 8d04d6b8-d110-45a3-b3bb-5a7b680ddabe
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: AddEntryList, AddEntryList method [Media Foundation], AddEntryList method [Media Foundation],IToc interface, IToc interface [Media Foundation],AddEntryList method, IToc.AddEntryList, IToc::AddEntryList, codecapi.itoc_addentrylist, mf.itoc_addentrylist, wmcodecdsp/IToc::AddEntryList
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
 - IToc.AddEntryList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IToc::AddEntryList


## -description


The <b>AddEntryList</b> method adds an entry list to the table of contents and assigns an index to the entry list.


## -parameters




### -param pEntryList [in]

Pointer to an <a href="https://msdn.microsoft.com/98052f26-7956-4973-ab86-428e7a355937">ITocEntryList</a> interface that represents the entry list to be added.


### -param pwEntryListIndex [out]

Receives the index of the added entry list.


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




<a href="https://msdn.microsoft.com/b12d38c7-b80e-4ca8-9ac5-a116100911d0">IToc</a>



<a href="https://msdn.microsoft.com/63137b67-dc00-48e7-88b0-2f7159c1d829">RemoveEntryListByIndex</a>
 

 

