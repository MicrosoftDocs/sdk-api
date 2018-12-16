---
UID: NF:vidcap.IKsTopologyInfo.get_Category
title: IKsTopologyInfo::get_Category
author: windows-sdk-content
description: The get_Category method returns one of the filter categories for this stream class driver.
old-location: dshow\ikstopologyinfo_get_category.htm
tech.root: DirectShow
ms.assetid: 1026ec92-1ccd-4658-b217-3dbc2ee9ca3a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IKsTopologyInfo interface [DirectShow],get_Category method, IKsTopologyInfo.get_Category, IKsTopologyInfo::get_Category, IKsTopologyInfoget_Category, dshow.ikstopologyinfo_get_category, get_Category, get_Category method [DirectShow], get_Category method [DirectShow],IKsTopologyInfo interface, vidcap/IKsTopologyInfo::get_Category
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
 - IKsTopologyInfo.get_Category
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKsTopologyInfo::get_Category


## -description


The <code>get_Category</code> method returns one of the filter categories for this stream class driver.


## -parameters




### -param dwIndex [in]

Index of the category GUID to retrieve. To find the number of categories, call the <a href="https://msdn.microsoft.com/en-us/library/Dd390154(v=VS.85).aspx">IKsTopologyInfo::get_NumCategories</a> method.


### -param pCategory [out]

Receives a GUID that defines the category. Microsoft provides standard categories in the header files Ks.h and Ksmedia.h.


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



<a href="https://msdn.microsoft.com/en-us/library/Dd390148(v=VS.85).aspx">IKsTopologyInfo Interface</a>
 

 

