---
UID: NF:mfobjects.IMFCollection.RemoveElement
title: IMFCollection::RemoveElement
author: windows-sdk-content
description: Removes an object from the collection.
old-location: mf\imfcollection_removeelement.htm
old-project: medfound
ms.assetid: 47f33235-6bb5-4103-82b4-87210b0e695c
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: 47f33235-6bb5-4103-82b4-87210b0e695c, IMFCollection interface [Media Foundation],RemoveElement method, IMFCollection.RemoveElement, IMFCollection::RemoveElement, RemoveElement, RemoveElement method [Media Foundation], RemoveElement method [Media Foundation],IMFCollection interface, mf.imfcollection_removeelement, mfobjects/IMFCollection::RemoveElement
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: MF_FILE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFCollection.RemoveElement
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCollection::RemoveElement


## -description



Removes an object from the collection.




## -parameters




### -param dwElementIndex [in]

Zero-based index of the object to remove. Objects are indexed in the order in which they were added to the collection.


### -param ppUnkElement [out]

Receives a pointer to the <b>IUnknown</b> interface of the object. The caller must release the interface. This parameter cannot be <b>NULL</b>, but the retrieved pointer value might be <b>NULL</b>.


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
 




## -see-also




<a href="https://msdn.microsoft.com/fec6aa17-2770-4f53-b36d-b94236093d23">IMFCollection</a>
 

 

