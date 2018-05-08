---
UID: NF:wmcodecdsp.IToc.GetEntryListCount
title: IToc::GetEntryListCount
author: windows-driver-content
description: The GetEntryListCount method retrieves the number of entry lists in the table of contents.
old-location: mf\itoc_getentrylistcount.htm
old-project: medfound
ms.assetid: 38348080-e188-4d58-8d46-dc954da398e6
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetEntryListCount, GetEntryListCount method [Media Foundation], GetEntryListCount method [Media Foundation],IToc interface, IToc interface [Media Foundation],GetEntryListCount method, IToc.GetEntryListCount, IToc::GetEntryListCount, codecapi.itoc_getentrylistcount, mf.itoc_getentrylistcount, wmcodecdsp/IToc::GetEntryListCount
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
-	IToc.GetEntryListCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IToc::GetEntryListCount


## -description


The <b>GetEntryListCount</b> method retrieves the number of entry lists in the table of contents.


## -parameters




### -param pwCount

Pointer to a <b>WORD</b> that receives the number of entry lists.


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




<a href="https://msdn.microsoft.com/5c457eb4-3034-40e3-93b6-e421c2e34bcf">GetEntryListByIndex</a>



<a href="https://msdn.microsoft.com/b12d38c7-b80e-4ca8-9ac5-a116100911d0">IToc</a>
 

 

