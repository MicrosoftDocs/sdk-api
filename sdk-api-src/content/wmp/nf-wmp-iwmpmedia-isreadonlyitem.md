---
UID: NF:wmp.IWMPMedia.isReadOnlyItem
title: IWMPMedia::isReadOnlyItem
author: windows-sdk-content
description: The isReadOnlyItem method retrieves a value indicating whether the attributes of the specified media item can be edited.
old-location: wmp\iwmpmedia_isreadonlyitem.htm
old-project: WMP
ms.assetid: d8b2dd45-3e3f-4325-b4d0-939abbc425e1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPMedia interface [Windows Media Player],isReadOnlyItem method, IWMPMedia.isReadOnlyItem, IWMPMedia2 interface [Windows Media Player],isReadOnlyItem method, IWMPMedia2::isReadOnlyItem, IWMPMedia3 interface [Windows Media Player],isReadOnlyItem method, IWMPMedia3::isReadOnlyItem, IWMPMedia::isReadOnlyItem, IWMPMediaisReadOnlyItem, isReadOnlyItem, isReadOnlyItem method [Windows Media Player], isReadOnlyItem method [Windows Media Player],IWMPMedia interface, isReadOnlyItem method [Windows Media Player],IWMPMedia2 interface, isReadOnlyItem method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_isreadonlyitem, wmp/IWMPMedia2::isReadOnlyItem, wmp/IWMPMedia3::isReadOnlyItem, wmp/IWMPMedia::isReadOnlyItem
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPMedia.isReadOnlyItem
 - IWMPMedia2.isReadOnlyItem
 - IWMPMedia3.isReadOnlyItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMedia::isReadOnlyItem


## -description



The <b>isReadOnlyItem</b> method retrieves a value indicating whether the attributes of the specified media item can be edited.




## -parameters




### -param bstrItemName [in]

<b>BSTR</b> containing the item name.


### -param pvarfIsReadOnly [out]

Pointer to a <b>VARIANT_BOOL</b> that specifies whether the attributes are read-only.


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



If an attribute is read-only, then it cannot be set with the <b>setItemInfo</b> method. Note that this method may return different values for a particular attribute when used with different versions of Windows Media Player.

Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

<b>Windows Media Player 10 Mobile:</b> This method always retrieves a <b>VARIANT_BOOL</b> set to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/919fe92f-9519-4229-8097-4970a8f6cc25">IWMPMedia::setItemInfo</a>
 

 

