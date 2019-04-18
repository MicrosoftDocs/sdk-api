---
UID: NF:adhoc.IEnumDot11AdHocInterfaces.Next
title: IEnumDot11AdHocInterfaces::Next (adhoc.h)
author: windows-sdk-content
description: Gets the specified number of elements from the sequence and advances the current position by the number of items retrieved.
old-location: nwifi\ienumdot11adhocinterfaces_next.htm
tech.root: NativeWiFi
ms.assetid: 2c20e215-a4ef-456e-ba19-0d9268279bf3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumDot11AdHocInterfaces interface [NativeWIFI],Next method, IEnumDot11AdHocInterfaces.Next, IEnumDot11AdHocInterfaces::Next, Next, Next method [NativeWIFI], Next method [NativeWIFI],IEnumDot11AdHocInterfaces interface, adhoc/IEnumDot11AdHocInterfaces::Next, nwifi.ienumdot11adhocinterfaces_next
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IEnumDot11AdHocInterfaces.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumDot11AdHocInterfaces::Next


## -description


Gets the specified number of elements from the sequence and advances the current position by the number of items retrieved. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.



## -parameters




### -param cElt [in]

The number of elements requested. 



### -param rgElt [out]

A pointer to a variable that, on successful return, points to an array of pointers to <a href="https://msdn.microsoft.com/a4a73ff8-e24a-4f44-9205-c60699d1c27d">IDot11AdHocInterface</a> interfaces. The array is of size <i>cElt</i>.


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




<a href="https://msdn.microsoft.com/c61bbe3a-ad02-4182-bf10-1ed5fe307bd4">IEnumDot11AdHocInterfaces</a>
 

 

