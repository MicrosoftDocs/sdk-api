---
UID: NF:vidcap.ISelector.get_SourceNodeId
title: ISelector::get_SourceNodeId
author: windows-sdk-content
description: The get_SourceNodeId method returns the index of the active source node.
old-location: dshow\iselector_get_sourcenodeid.htm
old-project: DirectShow
ms.assetid: ae2b0e1a-1527-4634-b2f9-47c9519b55a6
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: ISelector interface [DirectShow],get_SourceNodeId method, ISelector.get_SourceNodeId, ISelector::get_SourceNodeId, ISelectorget_SourceNodeId, dshow.iselector_get_sourcenodeid, get_SourceNodeId, get_SourceNodeId method [DirectShow], get_SourceNodeId method [DirectShow],ISelector interface, vidcap/ISelector::get_SourceNodeId
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AVISTREAMINFOW, *LPAVISTREAMINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - ISelector.get_SourceNodeId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ISelector::get_SourceNodeId


## -description


The <code>get_SourceNodeId</code> method returns the index of the active source node.


## -parameters




### -param pdwPinId [out]

Receives the index of the source node that is currently active.


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



<a href="https://msdn.microsoft.com/bd6e028c-ed6d-4dad-a276-c59ba9d88e87">ISelector Interface</a>
 

 

