---
UID: NF:vidcap.ISelector.get_NumSources
title: ISelector::get_NumSources (vidcap.h)
author: windows-sdk-content
description: The get_NumSources method returns the number of source nodes connected to the selector node.
old-location: dshow\iselector_get_numsources.htm
tech.root: DirectShow
ms.assetid: ff04e32f-7902-417e-b0d4-125914928679
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISelector interface [DirectShow],get_NumSources method, ISelector.get_NumSources, ISelector::get_NumSources, ISelectorget_NumSources, dshow.iselector_get_numsources, get_NumSources, get_NumSources method [DirectShow], get_NumSources method [DirectShow],ISelector interface, vidcap/ISelector::get_NumSources
ms.topic: method
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - ISelector.get_NumSources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISelector::get_NumSources


## -description


The <code>get_NumSources</code> method returns the number of source nodes connected to the selector node.


## -parameters




### -param pdwNumSources [out]

Receives the number of source nodes.


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377075(v=VS.85).aspx">ISelector Interface</a>
 

 

