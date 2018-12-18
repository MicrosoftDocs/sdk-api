---
UID: NF:wmp.IWMPCdromCollection.get_count
title: IWMPCdromCollection::get_count
author: windows-sdk-content
description: The get_count method retrieves the number of available CD and DVD drives on the system.
old-location: wmp\iwmpcdromcollection_get_count.htm
tech.root: WMP
ms.assetid: 0e0c73b3-463c-43de-b1b8-5644a377bfd1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPCdromCollection interface [Windows Media Player],get_count method, IWMPCdromCollection.get_count, IWMPCdromCollection::get_count, IWMPCdromCollectionget_count, get_count, get_count method [Windows Media Player], get_count method [Windows Media Player],IWMPCdromCollection interface, wmp.iwmpcdromcollection_get_count, wmp/IWMPCdromCollection::get_count
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
 - IWMPCdromCollection.get_count
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPCdromCollection::get_count


## -description



The <b>get_count</b> method retrieves the number of available CD and DVD drives on the system.




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



To retrieve the value of this property, read access to the library is required. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

DVD drives are counted exactly like CD drives. However, the Windows Media Player ActiveX control only supports DVD functionality for Windows XP or later. Typically, DVD drives can play CD media, but CD drives cannot play DVD media.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>long</b> set to 0.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563097(v=VS.85).aspx">IWMPCdromCollection Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563651(v=VS.85).aspx">IWMPSettings2::get_mediaAccessRights</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563652(v=VS.85).aspx">IWMPSettings2::requestMediaAccessRights</a>
 

 

