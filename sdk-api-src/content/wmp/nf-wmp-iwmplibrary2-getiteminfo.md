---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# IWMPLibrary2::getItemInfo


## -description


The <b>getItemInfo</b> method retrieves the value of the <b>LibraryID</b> attribute.


## -parameters




### -param bstrItemName [in]

<b>BSTR</b> containing the attribute name. Set the value of this parameter to "LibraryID".


### -param pbstrVal [out]

Pointer to a <b>BSTR</b> that receives the value of the <b>LibraryID</b> attribute.


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



The <b>LibraryID</b> attribute retrieved by this method is the same as the <b>LibraryID</b> attribute that <a href="https://msdn.microsoft.com/ee964f68-d44c-4e66-908b-09070a96d96f">IWMPMedia::getItemInfo</a> retrieves for each media item in the library.




## -see-also




<a href="https://msdn.microsoft.com/028250e7-7415-4643-b798-af0112c1ea93">IWMPLibrary2</a>
 

 

