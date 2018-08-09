---
UID: NF:wmcodecdsp.IToc.RemoveEntryListByIndex
title: IToc::RemoveEntryListByIndex
author: windows-sdk-content
description: The RemoveEntryListByIndex method removes an entry list, specified by an index, from the table of contents.
old-location: mf\itoc_removeentrylistbyindex.htm
old-project: medfound
ms.assetid: 63137b67-dc00-48e7-88b0-2f7159c1d829
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IToc interface [Media Foundation],RemoveEntryListByIndex method, IToc.RemoveEntryListByIndex, IToc::RemoveEntryListByIndex, RemoveEntryListByIndex, RemoveEntryListByIndex method [Media Foundation], RemoveEntryListByIndex method [Media Foundation],IToc interface, codecapi.itoc_removeentrylistbyindex, mf.itoc_removeentrylistbyindex, wmcodecdsp/IToc::RemoveEntryListByIndex
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFVideoDSPMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmvdspa.dll
api_name:
 - IToc.RemoveEntryListByIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IToc::RemoveEntryListByIndex


## -description


The <b>RemoveEntryListByIndex</b> method removes an entry list, specified by an index, from the table of contents.


## -parameters




### -param wEntryListIndex [in]

The index of the entry list to be removed.


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




<a href="https://msdn.microsoft.com/273e1c38-7f1a-4f04-b1a8-ba27b5babf94">AddEntryListByIndex</a>



<a href="https://msdn.microsoft.com/b12d38c7-b80e-4ca8-9ac5-a116100911d0">IToc</a>
 

 

