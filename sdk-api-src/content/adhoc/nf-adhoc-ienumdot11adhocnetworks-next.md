---
UID: NF:adhoc.IEnumDot11AdHocNetworks.Next
title: IEnumDot11AdHocNetworks::Next
author: windows-sdk-content
description: Gets the specified number of elements from the sequence and advances the current position by the number of items retrieved.
old-location: nwifi\ienumdot11adhocnetworks_next.htm
old-project: nativewifi
ms.assetid: a695c8dd-5bde-41ff-8214-046e0a8cc26f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnumDot11AdHocNetworks interface [NativeWIFI],Next method, IEnumDot11AdHocNetworks.Next, IEnumDot11AdHocNetworks::Next, Next, Next method [NativeWIFI], Next method [NativeWIFI],IEnumDot11AdHocNetworks interface, adhoc/IEnumDot11AdHocNetworks::Next, nwifi.ienumdot11adhocnetworks_next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IEnumDot11AdHocNetworks.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IEnumDot11AdHocNetworks::Next


## -description


Gets the specified number of elements from the sequence and advances the current position by the number of items retrieved. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.



## -parameters




### -param cElt [in]

The number of elements requested. 



### -param rgElt [out]

A pointer to the first element in an array of  <a href="https://msdn.microsoft.com/2736bb81-b66f-4c09-8c76-ca16f3eab192">IDot11AdHocNetwork</a> interfaces. The array is of size <i>cElt</i>. The array must exist and be of size <i>cElt</i> (at a minimum) before the <b>Next</b> method is called, although the array need not be initialized. Upon return, the previously existing array will contain pointers to <b>IDot11AdHocNetwork</b>  objects.


### -param pcEltFetched [out]

A pointer to a variable that specifies the number of elements returned in <i>rgElt</i>.


## -returns



Possible return values include, but are not limited to, the following.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
A specified interface is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate the memory required to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5818e921-86bc-4f96-9ecd-3cb9c9a1a488">IEnumDot11AdHocNetworks</a>
 

 

