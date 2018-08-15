---
UID: NF:wmp.IWMPStringCollection2.getItemInfo
title: IWMPStringCollection2::getItemInfo
author: windows-sdk-content
description: The getItemInfo method retrieves the string corresponding to the specified string collection item index and name.
old-location: wmp\iwmpstringcollection2_getiteminfo.htm
old-project: WMP
ms.assetid: 1915d71f-aca3-4943-a4da-ed8f2fa3f46d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPStringCollection2 interface [Windows Media Player],getItemInfo method, IWMPStringCollection2.getItemInfo, IWMPStringCollection2::getItemInfo, IWMPStringCollection2getItemInfo, getItemInfo, getItemInfo method [Windows Media Player], getItemInfo method [Windows Media Player],IWMPStringCollection2 interface, wmp.iwmpstringcollection2_getiteminfo, wmp/IWMPStringCollection2::getItemInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
 - IWMPStringCollection2.getItemInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPStringCollection2::getItemInfo


## -description



The <b>getItemInfo</b> method retrieves the string corresponding to the specified string collection item index and name.




## -parameters




### -param lCollectionIndex [in]

A <b>long</b> specifying the zero-based index of the string collection item from which to get the attribute.


### -param bstrItemName [in]

<b>BSTR</b> containing the attribute name.


### -param pbstrValue [out]

Pointer to a <b>BSTR</b> that receives the string. For attributes whose underlying value is <b>Boolean</b>, it returns the string "true" or "false".


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



To retrieve attributes with multiple values and attributes with complex values, use the <b>getItemInfoByType</b> method.

To use this method, read access to the library is required. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/7aeaf549-3c60-4dd8-9e46-6bab357f4960">IWMPStringCollection2 Interface</a>



<a href="https://msdn.microsoft.com/ff395caf-9b5a-41e0-94c6-4a5eb96281ca">IWMPStringCollection2::getItemInfoByType</a>
 

 

