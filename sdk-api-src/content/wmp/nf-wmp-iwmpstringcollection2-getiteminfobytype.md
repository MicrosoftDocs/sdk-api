---
UID: NF:wmp.IWMPStringCollection2.getItemInfoByType
title: IWMPStringCollection2::getItemInfoByType
author: windows-sdk-content
description: The getItemInfoByType method retrieves the value corresponding to the specified string collection item index, name, language, and attribute index.
old-location: wmp\iwmpstringcollection2_getiteminfobytype.htm
old-project: WMP
ms.assetid: ff395caf-9b5a-41e0-94c6-4a5eb96281ca
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: IWMPStringCollection2 interface [Windows Media Player],getItemInfoByType method, IWMPStringCollection2.getItemInfoByType, IWMPStringCollection2::getItemInfoByType, IWMPStringCollection2getItemInfoByType, getItemInfoByType, getItemInfoByType method [Windows Media Player], getItemInfoByType method [Windows Media Player],IWMPStringCollection2 interface, wmp.iwmpstringcollection2_getiteminfobytype, wmp/IWMPStringCollection2::getItemInfoByType
ms.prod: windows
ms.technology: windows-sdk
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
 - IWMPStringCollection2.getItemInfoByType
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPStringCollection2::getItemInfoByType


## -description



The <b>getItemInfoByType</b> method retrieves the value corresponding to the specified string collection item index, name, language, and attribute index.




## -parameters




### -param lCollectionIndex [in]

A <b>long</b> specifying the zero-based index of the string collection item from which to get the attribute.


### -param bstrType [in]

<b>BSTR</b> containing the attribute name.


### -param bstrLanguage [in]

<b>BSTR</b> containing the language. If the value is set to null or "" (empty string) the current locale string is used. Otherwise, the value must be a valid RFC 1766 language string such as "en-us".


### -param lAttributeIndex [in]

A <b>long</b> containing the zero-based index of the attribute.


### -param pvarValue [out]

Pointer to a <b>VARIANT</b> that receives the returned value.


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



This method supports attributes with multiple values and attributes with complex values. The <b>getItemInfo</b> method does not support attributes with multiple values or attributes with complex values.

By passing the value "ChildList" in the <i>bstrType</i> parameter, you can retrieve a new string collection that contains the children of one of the items in the parent string collection. For instance, if the parent collection contains a list of AlbumIDs, you can use this method to obtain a child string collection that contains all the tracks for one of the albums. This approach is faster and more efficient than calling the <b>IWMPMediaCollection2::getStringCollectionByQuery</b> method twice; once to get a collection of AlbumIDs, and a second time to get a collection of titles for a particular AlbumID. To use ChildList in the way just described, the parent string collection must be obtained from a media collection through <b>IWMPLibraryServices</b>, and not by using the <b>IWMPCore::get_mediaCollection</b> method.

When using ChildList, pass the value "ChildList" in the <i>bstrType</i> parameter, and the value 0 in the <i>lAttributeIndex</i> parameter. You can call <b>QueryInterface</b> on the <b>VARIANT</b> that is returned to obtain an <b>IWMPStringCollection2</b> interface, from which you can access the child list.

To use this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/0412d91a-11a7-434c-8717-a71d85655679">AlbumID Attribute</a>



<a href="https://msdn.microsoft.com/9ed6d02e-15ca-425f-8642-e32a5adfaa55">IWMPLibraryServices Interface</a>



<a href="https://msdn.microsoft.com/070bc947-bf2b-4c06-9ffa-6a23625d178a">IWMPMediaCollection2::getStringCollectionByQuery</a>



<a href="https://msdn.microsoft.com/7aeaf549-3c60-4dd8-9e46-6bab357f4960">IWMPStringCollection2 Interface</a>



<a href="https://msdn.microsoft.com/1915d71f-aca3-4943-a4da-ed8f2fa3f46d">IWMPStringCollection2::getItemInfo</a>
 

 

