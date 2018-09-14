---
UID: NF:adhoc.IEnumDot11AdHocSecuritySettings.Next
title: IEnumDot11AdHocSecuritySettings::Next
author: windows-sdk-content
description: Gets the specified number of elements from the sequence and advances the current position by the number of items retrieved.
old-location: nwifi\ienumdot11adhocsecuritysettings_next.htm
tech.root: NativeWiFi
ms.assetid: 77101f70-de5d-4db9-a59d-5b07f386c0b7
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IEnumDot11AdHocSecuritySettings interface [NativeWIFI],Next method, IEnumDot11AdHocSecuritySettings.Next, IEnumDot11AdHocSecuritySettings::Next, Next, Next method [NativeWIFI], Next method [NativeWIFI],IEnumDot11AdHocSecuritySettings interface, adhoc/IEnumDot11AdHocSecuritySettings::Next, nwifi.ienumdot11adhocsecuritysettings_next
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IEnumDot11AdHocSecuritySettings.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumDot11AdHocSecuritySettings::Next


## -description


Gets the specified number of elements from the sequence and advances the current position by the number of items retrieved. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.


## -parameters




### -param cElt [in]

The number of elements requested. 



### -param rgElt [out]

A pointer to a variable that, on successful return, points an array of pointers to <a href="https://msdn.microsoft.com/55b78a98-ad25-4646-b325-73d770d602b3">IDot11AdHocSecuritySettings</a>  interfaces. The array is of size <i>cElt</i>. 


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




<a href="https://msdn.microsoft.com/137abd1b-997d-4003-9fef-8db56b273149">IEnumDot11AdHocSecuritySettings</a>
 

 

