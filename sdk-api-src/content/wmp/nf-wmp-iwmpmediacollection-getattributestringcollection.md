---
UID: NF:wmp.IWMPMediaCollection.getAttributeStringCollection
title: IWMPMediaCollection::getAttributeStringCollection
author: windows-sdk-content
description: The getAttributeStringCollection method retrieves a pointer to an IWMPStringCollection interface. This interface represents the set of all values for a given attribute within a given media type.
old-location: wmp\iwmpmediacollection_getattributestringcollection.htm
tech.root: WMP
ms.assetid: c3699acb-58a1-4efa-a42c-c84534abca96
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPMediaCollection interface [Windows Media Player],getAttributeStringCollection method, IWMPMediaCollection.getAttributeStringCollection, IWMPMediaCollection::getAttributeStringCollection, IWMPMediaCollectiongetAttributeStringCollection, getAttributeStringCollection, getAttributeStringCollection method [Windows Media Player], getAttributeStringCollection method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_getattributestringcollection, wmp/IWMPMediaCollection::getAttributeStringCollection
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
 - IWMPMediaCollection.getAttributeStringCollection
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
- IWMPMediaCollection.getAttributeStringCollection
: 
---

# IWMPMediaCollection::getAttributeStringCollection


## -description



The <b>getAttributeStringCollection</b> method retrieves a pointer to an <b>IWMPStringCollection</b> interface. This interface represents the set of all values for a given attribute within a given media type.




## -parameters




### -param bstrAttribute [in]

String containing the attribute for which the values are retrieved.


### -param bstrMediaType [in]

String containing the media type for which the values are retrieved.


### -param ppStringCollection [out]

Pointer to a pointer to an <b>IWMPStringCollection</b> interface for the retrieved values.


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



Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

For information about the attributes supported by Windows Media Player, see the <a href="https://msdn.microsoft.com/a333ee0d-8f74-4517-b4c7-b1d8f95df2fc">Attribute Reference</a> section.




## -see-also




<a href="https://msdn.microsoft.com/bf975a30-dfb1-4994-9095-510a6b997aff">IWMPMediaCollection Interface</a>



<a href="https://msdn.microsoft.com/8cdabea9-7e37-4e63-9d6c-b6f63aa536ea">IWMPStringCollection Interface</a>
 

 

