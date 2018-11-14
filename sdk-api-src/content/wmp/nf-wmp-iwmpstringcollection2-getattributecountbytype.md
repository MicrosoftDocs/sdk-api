---
UID: NF:wmp.IWMPStringCollection2.getAttributeCountByType
title: IWMPStringCollection2::getAttributeCountByType
author: windows-sdk-content
description: The getAttributeCountByType method retrieves the number of attributes associated with the specified string collection index, attribute name, and language.
old-location: wmp\iwmpstringcollection2_getattributecountbytype.htm
tech.root: WMP
ms.assetid: 62e31749-2640-4b65-a8ee-47f3d3dd5485
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPStringCollection2 interface [Windows Media Player],getAttributeCountByType method, IWMPStringCollection2.getAttributeCountByType, IWMPStringCollection2::getAttributeCountByType, IWMPStringCollection2getAttributeCountByType, getAttributeCountByType, getAttributeCountByType method [Windows Media Player], getAttributeCountByType method [Windows Media Player],IWMPStringCollection2 interface, wmp.iwmpstringcollection2_getattributecountbytype, wmp/IWMPStringCollection2::getAttributeCountByType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
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
 - IWMPStringCollection2.getAttributeCountByType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmp.h
: 
- IWMPStringCollection2.getAttributeCountByType
: 
---

# IWMPStringCollection2::getAttributeCountByType


## -description



The <b>getAttributeCountByType</b> method retrieves the number of attributes associated with the specified string collection index, attribute name, and language.




## -parameters




### -param lCollectionIndex [in]

A <b>long</b> specifying the zero-based index of the string collection item from which to get the attribute.


### -param bstrType [in]

<b>BSTR</b> containing the name of the attribute.


### -param bstrLanguage [in]

<b>BSTR</b> containing the language. If the value is set to null or "" (empty string), the current locale string is used. Otherwise, the value must be a valid RFC 1766 language string such as "en-us".


### -param plCount [out]

Pointer to a <b>long</b> that receives the count.


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



This method is used to determine the number of attributes corresponding to a particular attribute name for a given <b>StringCollection</b> item. Index numbers can then be passed to the fourth parameter of the <b>getItemInfoByType</b> method.

To use this method, read access to the library is required. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/7aeaf549-3c60-4dd8-9e46-6bab357f4960">IWMPStringCollection2 Interface</a>



<a href="https://msdn.microsoft.com/ff395caf-9b5a-41e0-94c6-4a5eb96281ca">IWMPStringCollection2::getItemInfoByType</a>
 

 

