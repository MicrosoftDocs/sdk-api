---
UID: NF:vidcap.ISelector.get_NumSources
title: ISelector::get_NumSources (vidcap.h)
description: The get_NumSources method returns the number of source nodes connected to the selector node.helpviewer_keywords: ["ISelector interface [DirectShow]","get_NumSources method","ISelector.get_NumSources","ISelector::get_NumSources","ISelectorget_NumSources","dshow.iselector_get_numsources","get_NumSources","get_NumSources method [DirectShow]","get_NumSources method [DirectShow]","ISelector interface","vidcap/ISelector::get_NumSources"]
old-location: dshow\iselector_get_numsources.htm
tech.root: DirectShow
ms.assetid: ff04e32f-7902-417e-b0d4-125914928679
ms.date: 12/05/2018
ms.keywords: ISelector interface [DirectShow],get_NumSources method, ISelector.get_NumSources, ISelector::get_NumSources, ISelectorget_NumSources, dshow.iselector_get_numsources, get_NumSources, get_NumSources method [DirectShow], get_NumSources method [DirectShow],ISelector interface, vidcap/ISelector::get_NumSources
f1_keywords:
- vidcap/ISelector.get_NumSources
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-iselector">ISelector Interface</a>
 

 

