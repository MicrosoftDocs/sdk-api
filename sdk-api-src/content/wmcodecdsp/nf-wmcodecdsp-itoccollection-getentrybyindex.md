---
UID: NF:wmcodecdsp.ITocCollection.GetEntryByIndex
title: ITocCollection::GetEntryByIndex
author: windows-sdk-content
description: The GetEntryByIndex method retrieves a table of contents, specified by an index, from the collection.
old-location: mf\itoccollection_getentrybyindex.htm
old-project: medfound
ms.assetid: 93bddd4d-8a58-46e6-9284-eaa70be2c5a4
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetEntryByIndex, GetEntryByIndex method [Media Foundation], GetEntryByIndex method [Media Foundation],ITocCollection interface, ITocCollection interface [Media Foundation],GetEntryByIndex method, ITocCollection.GetEntryByIndex, ITocCollection::GetEntryByIndex, codecapi.itoccollection_getentrybyindex, mf.itoccollection_getentrybyindex, wmcodecdsp/ITocCollection::GetEntryByIndex
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmvdspa.dll
api_name:
-	ITocCollection.GetEntryByIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ITocCollection::GetEntryByIndex


## -description


The <b>GetEntryByIndex</b> method retrieves a table of contents, specified by an index, from the collection.


## -parameters




### -param dwEntryIndex [in]

Specifies the index of the table of contents to retrieve.


### -param ppToc [out]

Pointer to a variable that receives a pointer to an <a href="https://msdn.microsoft.com/b12d38c7-b80e-4ca8-9ac5-a116100911d0">IToc</a> interface that represents the table of contents.


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




<a href="https://msdn.microsoft.com/10d6fc04-4444-4a47-911f-3d5bec548e28">ITocCollection</a>
 

 

