---
UID: NF:wmcodecdsp.ITocCollection.GetEntryCount
title: ITocCollection::GetEntryCount (wmcodecdsp.h)
author: windows-sdk-content
description: The GetEntryCount method retrieves the number of tables of contents in the collection.
old-location: mf\itoccollection_getentrycount.htm
tech.root: medfound
ms.assetid: 494efcde-cab3-4e72-9bc6-1df61f125f62
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetEntryCount, GetEntryCount method [Media Foundation], GetEntryCount method [Media Foundation],ITocCollection interface, ITocCollection interface [Media Foundation],GetEntryCount method, ITocCollection.GetEntryCount, ITocCollection::GetEntryCount, codecapi.itoccollection_getentrycount, mf.itoccollection_getentrycount, wmcodecdsp/ITocCollection::GetEntryCount
ms.topic: method
f1_keywords: 
 - "wmcodecdsp/ITocCollection.GetEntryCount"
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
 - ITocCollection.GetEntryCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



In the context of an <a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoccollection">ITocCollection</a> interface, the word <i>entry</i> refers to an indivdual table of contents. That meaning of the word <i>entry</i> is in contrast to its meaning in the context of other interfaces in the TOC Parser technology. For example, in the context of an <a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc">IToc</a> interface, the word <i>entry</i> refers to a block of information, in a table of contents, that represents a section of a video file. 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/ee264253(v=vs.85)">GetEntryByIndex</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoccollection">ITocCollection</a>
 

 

