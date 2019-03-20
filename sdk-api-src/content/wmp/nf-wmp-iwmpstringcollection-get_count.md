---
UID: NF:wmp.IWMPStringCollection.get_count
title: IWMPStringCollection::get_count (wmp.h)
author: windows-sdk-content
description: The get_count method retrieves the number of items in the string collection.
old-location: wmp\iwmpstringcollection_get_count.htm
tech.root: WMP
ms.assetid: 97865752-e4bf-4f91-b481-22d9c8b3e090
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPStringCollection interface [Windows Media Player],get_count method, IWMPStringCollection.get_count, IWMPStringCollection::get_count, IWMPStringCollectionget_count, get_count, get_count method [Windows Media Player], get_count method [Windows Media Player],IWMPStringCollection interface, wmp.iwmpstringcollection_get_count, wmp/IWMPStringCollection::get_count
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
req.target-min-winversvr: 
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
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPStringCollection.get_count
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPStringCollection::get_count


## -description



The <b>get_count</b> method retrieves the number of items in the string collection.




## -parameters




### -param plCount [out]

Pointer to a <b>long</b> containing the count.


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



To retrieve the value of this method, read access to the library is required. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563651(v=VS.85).aspx">IWMPSettings2::get_mediaAccessRights</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563652(v=VS.85).aspx">IWMPSettings2::requestMediaAccessRights</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563686(v=VS.85).aspx">IWMPStringCollection Interface</a>
 

 

