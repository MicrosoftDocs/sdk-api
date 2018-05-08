---
UID: NF:wmsdkidl.IWMHeaderInfo3.DeleteAttribute
title: IWMHeaderInfo3::DeleteAttribute
author: windows-driver-content
description: The DeleteAttribute method removes an attribute from the file header.
old-location: wmformat\iwmheaderinfo3_deleteattribute.htm
old-project: wmformat
ms.assetid: a69da90f-c8c5-4bf7-a1d8-7031aa9d1704
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: DeleteAttribute, DeleteAttribute method [windows Media Format], DeleteAttribute method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo3 interface [windows Media Format],DeleteAttribute method, IWMHeaderInfo3.DeleteAttribute, IWMHeaderInfo3::DeleteAttribute, IWMHeaderInfo3DeleteAttribute, wmformat.iwmheaderinfo3_deleteattribute, wmsdkidl/IWMHeaderInfo3::DeleteAttribute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMHeaderInfo3.DeleteAttribute
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMHeaderInfo3::DeleteAttribute


## -description



The <b>DeleteAttribute</b> method removes an attribute from the file header.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number for which the attribute applies. Setting this value to zero indicates a file-level attribute.


### -param wIndex [in]

<b>WORD</b> containing the index of the attribute to be deleted.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not implemented on a reader object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
<i>wStreamNum</i> is not a valid stream number, or there is not an attribute at <i>wIndex</i>.

</td>
</tr>
</table>
 




## -remarks



You can use 0xFFFF for the stream number to specify an attribute using its global index. Global index values range from 0 to one less than the count of attributes received from a call to <a href="https://msdn.microsoft.com/8c56d7b6-4f59-450e-938c-b7d0bd37ea08">IWMHeaderInfo3::GetAttributeCountEx</a> where the stream number was set to 0xFFFF.

When deleting multiple attributes, you should do so in descending order by index value. For convenience, this is the order in which index values are retrieved by <a href="https://msdn.microsoft.com/15c8f0c2-f2d4-441a-b6a9-774da820d03c">IWMHeaderInfo3::GetAttributeIndices</a>.




## -see-also




<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3 Interface</a>
 

 

