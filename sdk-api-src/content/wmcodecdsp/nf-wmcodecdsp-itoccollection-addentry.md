---
UID: NF:wmcodecdsp.ITocCollection.AddEntry
title: ITocCollection::AddEntry
author: windows-sdk-content
description: The AddEntry method adds an individual table of contents to the collection and assigns an index to the added table of contents.
old-location: mf\itoccollection_addentry.htm
tech.root: medfound
ms.assetid: b4d4e40b-151b-4217-81c8-1eaa8336407d
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AddEntry, AddEntry method [Media Foundation], AddEntry method [Media Foundation],ITocCollection interface, ITocCollection interface [Media Foundation],AddEntry method, ITocCollection.AddEntry, ITocCollection::AddEntry, codecapi.itoccollection_addentry, mf.itoccollection_addentry, wmcodecdsp/ITocCollection::AddEntry
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
 - ITocCollection.AddEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITocCollection::AddEntry


## -description


The <b>AddEntry</b> method adds an individual table of contents  to the collection and assigns an index to the added table of contents.


## -parameters




### -param pToc [in]

Pointer to an <a href="https://msdn.microsoft.com/b12d38c7-b80e-4ca8-9ac5-a116100911d0">IToc</a> interface that represents the table of contents to be added.


### -param pdwEntryIndex [out]

Pointer to a <b>DWORD</b> that receives the index of the added table of contents.


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
 

 

