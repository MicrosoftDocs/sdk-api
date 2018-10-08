---
UID: NF:mfobjects.IMFAttributes.GetItemByIndex
title: IMFAttributes::GetItemByIndex
author: windows-sdk-content
description: Retrieves an attribute at the specified index.
old-location: mf\imfattributes_getitembyindex.htm
tech.root: medfound
ms.assetid: 1290bc45-fcac-4379-b26c-e67ef678f193
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: 1290bc45-fcac-4379-b26c-e67ef678f193, GetItemByIndex, GetItemByIndex method [Media Foundation], GetItemByIndex method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetItemByIndex method, IMFAttributes.GetItemByIndex, IMFAttributes::GetItemByIndex, mf.imfattributes_getitembyindex, mfobjects/IMFAttributes::GetItemByIndex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFAttributes.GetItemByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAttributes::GetItemByIndex


## -description



Retrieves an attribute at the specified index.




## -parameters




### -param unIndex [in]

Index of the attribute to retrieve. To get the number of attributes, call <a href="https://msdn.microsoft.com/5f511d5c-249c-4311-8380-a932a755eaaf">IMFAttributes::GetCount</a>.


### -param pguidKey [out]

Receives the GUID that identifies this attribute.


### -param pValue [in, out]

Pointer to a <b>PROPVARIANT</b> that receives the value. This parameter can be <b>NULL</b>. If it is not <b>NULL</b>, the method fills the <b>PROPVARIANT</b> with a copy of the attribute value. Call <b>PropVariantClear</b> to free the memory allocated by this method.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid index.

</td>
</tr>
</table>
 




## -remarks



To enumerate all of an object's attributes in a thread-safe way, do the following:

<ol>
<li>
Call <a href="https://msdn.microsoft.com/6ec7aed3-7dbc-4aa4-92d5-646aee757db7">IMFAttributes::LockStore</a> to prevent another thread from adding or deleting attributes.

</li>
<li>
Call <a href="https://msdn.microsoft.com/5f511d5c-249c-4311-8380-a932a755eaaf">IMFAttributes::GetCount</a> to find the number of attributes.

</li>
<li>
Call <b>GetItemByIndex</b> to get each attribute by index.

</li>
<li>
Call <a href="https://msdn.microsoft.com/65e35864-868a-4ae9-86ed-772a2b2daeb6">IMFAttributes::UnlockStore</a> to unlock the attribute store.

</li>
</ol>
This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>
 

 

