---
UID: NF:vidcap.IKsTopologyInfo.get_NumCategories
title: IKsTopologyInfo::get_NumCategories
author: windows-sdk-content
description: The get_NumCategories method returns the number of categories for this filter.
old-location: dshow\ikstopologyinfo_get_numcategories.htm
tech.root: DirectShow
ms.assetid: 86bbe461-37c1-4dbc-bebd-fa8784d49083
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IKsTopologyInfo interface [DirectShow],get_NumCategories method, IKsTopologyInfo.get_NumCategories, IKsTopologyInfo::get_NumCategories, IKsTopologyInfoget_NumCategories, dshow.ikstopologyinfo_get_numcategories, get_NumCategories, get_NumCategories method [DirectShow], get_NumCategories method [DirectShow],IKsTopologyInfo interface, vidcap/IKsTopologyInfo::get_NumCategories
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IKsTopologyInfo.get_NumCategories
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKsTopologyInfo::get_NumCategories


## -description


The <code>get_NumCategories</code> method returns the number of categories for this filter.


## -parameters




### -param pdwNumCategories [out]

Receives the number of categories.


## -returns



The method returns an HRES<b></b>ULT. Possible values include, but are not limited to, those in the following table.

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



<a href="https://msdn.microsoft.com/en-us/library/Dd390148(v=VS.85).aspx">IKsTopologyInfo Interface</a>
 

 

