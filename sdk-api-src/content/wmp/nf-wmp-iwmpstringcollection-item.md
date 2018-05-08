---
UID: NF:wmp.IWMPStringCollection.item
title: IWMPStringCollection::item
author: windows-driver-content
description: The item method retrieves the string at the given index.
old-location: wmp\iwmpstringcollection_item.htm
old-project: WMP
ms.assetid: 05e7fd0c-1226-4680-a9aa-543111fd2bdf
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IWMPStringCollection interface [Windows Media Player],item method, IWMPStringCollection.item, IWMPStringCollection::item, IWMPStringCollectionitem, item, item method [Windows Media Player], item method [Windows Media Player],IWMPStringCollection interface, wmp.iwmpstringcollection_item, wmp/IWMPStringCollection::item
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPStringCollection.item
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPStringCollection::item


## -description



The <b>item</b> method retrieves the string at the given index.




## -parameters




### -param lIndex [in]

<b>long</b> containing the index.


### -param pbstrString [out]

Pointer to a <b>BSTR</b> containing the string.


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



The <b>IWMPStringCollection</b> interface is used to retrieve the set of values available for an attribute. For example, the <b>IWMPMediaCollection::getAttributeStringCollection</b> method can be used to retrieve a pointer to an <b>IWMPStringCollection</b> interface representing all the values for the Genre attribute within the Audio media type. The <b>item</b> method can then be used to iterate through all of the possible values for the Genre attribute.

To use this method, read access to the library is required. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/c3699acb-58a1-4efa-a42c-c84534abca96">IWMPMediaCollection::getAttributeStringCollection</a>



<a href="https://msdn.microsoft.com/07ca80a3-5175-4b1f-b83c-0df41a010cbf">IWMPSettings2::get_mediaAccessRights</a>



<a href="https://msdn.microsoft.com/925a4c0b-d613-4248-a341-bfc51d02cb85">IWMPSettings2::requestMediaAccessRights</a>



<a href="https://msdn.microsoft.com/8cdabea9-7e37-4e63-9d6c-b6f63aa536ea">IWMPStringCollection Interface</a>
 

 

