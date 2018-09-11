---
UID: NF:wmcodecdsp.IToc.GetEntryListByIndex
title: IToc::GetEntryListByIndex
author: windows-sdk-content
description: The GetEntryListByIndex method retrieves an entry list, specified by an index, from the table of contents.
old-location: mf\itoc_getentrylistbyindex.htm
tech.root: medfound
ms.assetid: 5c457eb4-3034-40e3-93b6-e421c2e34bcf
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetEntryListByIndex, GetEntryListByIndex method [Media Foundation], GetEntryListByIndex method [Media Foundation],IToc interface, IToc interface [Media Foundation],GetEntryListByIndex method, IToc.GetEntryListByIndex, IToc::GetEntryListByIndex, codecapi.itoc_getentrylistbyindex, mf.itoc_getentrylistbyindex, wmcodecdsp/IToc::GetEntryListByIndex
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
 - IToc.GetEntryListByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IToc::GetEntryListByIndex


## -description


The <b>GetEntryListByIndex</b> method retrieves an entry list, specified by an index, from the table of contents.


## -parameters




### -param wEntryListIndex [in]

The index of the entry list to retrieve.


### -param ppEntryList [out]

Pointer to a variable that receives a pointer to an <a href="https://msdn.microsoft.com/98052f26-7956-4973-ab86-428e7a355937">ITocEntryList</a> interface.


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
 

 

