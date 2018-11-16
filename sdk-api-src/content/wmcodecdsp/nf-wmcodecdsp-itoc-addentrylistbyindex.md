---
UID: NF:wmcodecdsp.IToc.AddEntryListByIndex
title: IToc::AddEntryListByIndex
author: windows-sdk-content
description: The AddEntryListByIndex method adds an entry list to the table of contents and associates a caller-supplied index with the entry list.
old-location: mf\itoc_addentrylistbyindex.htm
tech.root: medfound
ms.assetid: 273e1c38-7f1a-4f04-b1a8-ba27b5babf94
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AddEntryListByIndex, AddEntryListByIndex method [Media Foundation], AddEntryListByIndex method [Media Foundation],IToc interface, IToc interface [Media Foundation],AddEntryListByIndex method, IToc.AddEntryListByIndex, IToc::AddEntryListByIndex, codecapi.itoc_addentrylistbyindex, mf.itoc_addentrylistbyindex, wmcodecdsp/IToc::AddEntryListByIndex
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
 - IToc.AddEntryListByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmcodecdsp.h
: 
- IToc.AddEntryListByIndex
: 
---

# IToc::AddEntryListByIndex


## -description


The <b>AddEntryListByIndex</b> method adds an entry list to the table of contents and associates a caller-supplied index with the entry list.


## -parameters




### -param wEntryListIndex [in]

The index, specified by the caller, to be associated with the entry list.


### -param pEntryList [in]

Pointer to an <a href="https://msdn.microsoft.com/98052f26-7956-4973-ab86-428e7a355937">ITocEntryList</a> interface that represents the entry list to be added.


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
 

 

