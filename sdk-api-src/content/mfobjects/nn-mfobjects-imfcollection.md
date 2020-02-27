---
UID: NN:mfobjects.IMFCollection
title: IMFCollection (mfobjects.h)
description: Represents a generic collection of IUnknown pointers.
old-location: mf\imfcollection.htm
tech.root: medfound
ms.assetid: fec6aa17-2770-4f53-b36d-b94236093d23
ms.date: 12/05/2018
ms.keywords: IMFCollection, IMFCollection interface [Media Foundation], IMFCollection interface [Media Foundation],described, fec6aa17-2770-4f53-b36d-b94236093d23, mf.imfcollection, mfobjects/IMFCollection
f1_keywords:
- mfobjects/IMFCollection
dev_langs:
- c++
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFCollection interface


## -description


Represents a generic collection of <b>IUnknown</b> pointers.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCollection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-addelement">AddElement</a>
</td>
<td align="left" width="63%">
Adds an object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement">GetElement</a>
</td>
<td align="left" width="63%">
Retrieves an object in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelementcount">GetElementCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-insertelementat">InsertElementAt</a>
</td>
<td align="left" width="63%">
Adds an object at the specified index in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-removeallelements">RemoveAllElements</a>
</td>
<td align="left" width="63%">
Removes all items from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-removeelement">RemoveElement</a>
</td>
<td align="left" width="63%">
Removes an object from the collection.

</td>
</tr>
</table> 


## -remarks



To create an empty collection object, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatecollection">MFCreateCollection</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

