---
UID: NF:wmp.IWMPMedia3.getItemInfoByType
title: IWMPMedia3::getItemInfoByType
author: windows-sdk-content
description: The getItemInfoByType method retrieves the value of the attribute corresponding to the specified attribute type and index.
old-location: wmp\iwmpmedia3_getiteminfobytype.htm
tech.root: WMP
ms.assetid: 2a77029b-fbae-49af-bd91-c688c11b3b16
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPMedia3 interface [Windows Media Player],getItemInfoByType method, IWMPMedia3.getItemInfoByType, IWMPMedia3::getItemInfoByType, IWMPMedia3getItemInfoByType, getItemInfoByType, getItemInfoByType method [Windows Media Player], getItemInfoByType method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia3_getiteminfobytype, wmp/IWMPMedia3::getItemInfoByType
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
 - IWMPMedia3.getItemInfoByType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPMedia3::getItemInfoByType


## -description



The <b>getItemInfoByType</b> method retrieves the value of the attribute corresponding to the specified attribute type and index.




## -parameters




### -param bstrType [in]

<b>BSTR</b> containing the type.


### -param bstrLanguage [in]

<b>BSTR</b> containing the language. If the value is set to null or "" (empty string), the current locale string is used. Otherwise, the value must be a valid RFC 1766 language string such as "en-us".


### -param lIndex [in]

<b>long</b> containing the index.


### -param pvarValue [out]

Pointer to a <b>VARIANT</b> that contains the returned value.


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



This method retrieves the metadata for an individual digital media item or a media item that is part of a playlist.

This method supports attributes with multiple values and attributes with complex values. The <b>getItemInfo</b> method does not support attributes with multiple values and attributes with complex values.

The <b>attributeCount</b> method retrieves the number of attribute names available for a given media item. Index numbers can then be used with the <b>getAttributeName</b> method to determine the name of each available attribute. Individual attribute names can be passed to the <i>name</i> parameter of <b>getItemInfoByType</b>.

The <b>getAttributeCountByType</b> method returns the number of attributes that correspond to a particular attribute name for a given media item. Index numbers can then be passed to the <i>index</i> parameter of <b>getItemInfoByType</b>. This is useful when a media item has been categorized under multiple genres, for example.

The set of attributes available from sources other than the local library (remote libraries, portable devices, or CDs is defined by the other sources.

Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

<b>Windows Media Player 10 Mobile:</b> This method always returns E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/664a3148-3c78-41b0-85ba-9c2b3ac821d9">IWMPMedia3 Interface</a>



<a href="https://msdn.microsoft.com/86f5e67a-408f-4b93-b89a-12f42fd31966">IWMPMedia3::getAttributeCountByType</a>



<a href="https://msdn.microsoft.com/cb04e464-44dd-41ba-9296-f13aca9ef54e">IWMPMedia::getAttributeName</a>



<a href="https://msdn.microsoft.com/ee964f68-d44c-4e66-908b-09070a96d96f">IWMPMedia::getItemInfo</a>



<a href="https://msdn.microsoft.com/33e29da2-7439-41d1-9dd9-9b66e87aeb4b">IWMPMedia::get_attributeCount</a>
 

 

