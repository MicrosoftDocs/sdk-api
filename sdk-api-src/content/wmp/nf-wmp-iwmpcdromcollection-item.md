---
UID: NF:wmp.IWMPCdromCollection.item
title: IWMPCdromCollection::item (wmp.h)
author: windows-sdk-content
description: The item method retrieves a pointer to an IWMPCdrom interface at the given index.
old-location: wmp\iwmpcdromcollection_item.htm
tech.root: WMP
ms.assetid: 4604e53d-914f-4888-99c7-64d0683ac2e0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPCdromCollection interface [Windows Media Player],item method, IWMPCdromCollection.item, IWMPCdromCollection::item, IWMPCdromCollectionitem, item, item method [Windows Media Player], item method [Windows Media Player],IWMPCdromCollection interface, wmp.iwmpcdromcollection_item, wmp/IWMPCdromCollection::item
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
 - IWMPCdromCollection.item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPCdromCollection::item


## -description



The <b>item</b> method retrieves a pointer to an <b>IWMPCdrom</b> interface at the given index.




## -parameters




### -param lIndex [in]

<b>long</b> containing the index.


### -param ppItem [out]

Pointer to a pointer to an <b>IWMPCdrom</b> interface.


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



To use this method, read access to the library is required. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563080(v=VS.85).aspx">IWMPCdrom Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563097(v=VS.85).aspx">IWMPCdromCollection Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563099(v=VS.85).aspx">IWMPCdromCollection::get_count</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563109(v=VS.85).aspx">IWMPCdromCollection::get_driveSpecifier</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563571(v=VS.85).aspx">IWMPPlaylist::get_name</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563651(v=VS.85).aspx">IWMPSettings2::get_mediaAccessRights</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563652(v=VS.85).aspx">IWMPSettings2::requestMediaAccessRights</a>
 

 

