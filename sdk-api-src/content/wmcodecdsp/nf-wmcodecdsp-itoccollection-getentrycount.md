---
UID: NF:wmcodecdsp.ITocCollection.GetEntryCount
title: ITocCollection::GetEntryCount
author: windows-driver-content
description: The GetEntryCount method retrieves the number of tables of contents in the collection.
old-location: mf\itoccollection_getentrycount.htm
old-project: medfound
ms.assetid: 494efcde-cab3-4e72-9bc6-1df61f125f62
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetEntryCount, GetEntryCount method [Media Foundation], GetEntryCount method [Media Foundation],ITocCollection interface, ITocCollection interface [Media Foundation],GetEntryCount method, ITocCollection.GetEntryCount, ITocCollection::GetEntryCount, codecapi.itoccollection_getentrycount, mf.itoccollection_getentrycount, wmcodecdsp/ITocCollection::GetEntryCount
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
-	ITocCollection.GetEntryCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ITocCollection::GetEntryCount


## -description


The <b>GetEntryCount</b> method retrieves the number of tables of contents in the collection.


## -parameters




### -param pdwEntryCount [out]

Pointer to a <b>DWORD</b> that receives the number of tables of contents.


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
 




## -remarks



In the context of an <a href="https://msdn.microsoft.com/10d6fc04-4444-4a47-911f-3d5bec548e28">ITocCollection</a> interface, the word <i>entry</i> refers to an indivdual table of contents. That meaning of the word <i>entry</i> is in contrast to its meaning in the context of other interfaces in the TOC Parser technology. For example, in the context of an <a href="https://msdn.microsoft.com/b12d38c7-b80e-4ca8-9ac5-a116100911d0">IToc</a> interface, the word <i>entry</i> refers to a block of information, in a table of contents, that represents a section of a video file. 




## -see-also




<a href="https://msdn.microsoft.com/93bddd4d-8a58-46e6-9284-eaa70be2c5a4">GetEntryByIndex</a>



<a href="https://msdn.microsoft.com/10d6fc04-4444-4a47-911f-3d5bec548e28">ITocCollection</a>
 

 

