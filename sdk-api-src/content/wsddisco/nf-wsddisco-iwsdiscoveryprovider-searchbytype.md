---
UID: NF:wsddisco.IWSDiscoveryProvider.SearchByType
title: IWSDiscoveryProvider::SearchByType method
author: windows-driver-content
description: Initializes a search for WS-Discovery hosts by device type.
old-location: ncd\iwsdiscoveryprovider_searchbytype_method.htm
old-project: WsdApi
ms.assetid: bb1f2822-4d5d-4156-99e3-5a4528474953
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IWSDiscoveryProvider, IWSDiscoveryProvider interface, SearchByType method, IWSDiscoveryProvider::SearchByType, SearchByType method, SearchByType method, IWSDiscoveryProvider interface, SearchByType,IWSDiscoveryProvider.SearchByType, ncd.iwsdiscoveryprovider_searchbytype_method, wsddisco/IWSDiscoveryProvider::SearchByType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDiscoveryProvider.SearchByType
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDiscoveryProvider::SearchByType method


## -description


Initializes a search for <a href="http://go.microsoft.com/fwlink/p/?linkid=87841">WS-Discovery</a> hosts by device type.


## -parameters




### -param pTypesList [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/f573365d-100f-4df9-b1af-a484680436eb">WSD_NAME_LIST</a> structure that represents the list of discovery provider types to search for. May be <b>NULL</b>.


### -param pScopesList [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/86d77741-39c3-44bd-b072-d2d4eb99e488">WSD_URI_LIST</a> structure that represents the list of discovery provider scopes to search for. May be <b>NULL</b>.


### -param pszMatchBy [in, optional]

Matching rule used for scopes. May be <b>NULL</b>.


### -param pszTag [in, optional]

Optional identifier tag for this search.  May be <b>NULL</b>.


## -returns



Possible return values include, but are not limited to, the following:

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The length in characters of <i>pszMatchBy</i>  exceeds WSD_MAX_TEXT_LENGTH (8192) or the length in characters of  <i>pszTag</i> exceeds WSD_MAX_TEXT_LENGTH (8192).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
A callback interface has not been attached. You must call <a href="https://msdn.microsoft.com/3bb2aead-b082-4a2b-b4bf-97a1feb1e11e">Attach</a> before calling this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



<b>SearchByType</b> initiates a WS-Discovery <a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe</a> in an attempt to locate discovery hosts matching the provided criteria. This method allows matching by types, scopes, some combination of the two, or matching all discovery capable devices (when no scopes or types are provided). 

<i>pszMatchBy</i> should be provided if and only if <i>pScopesList</i> is also provided. This call may result in one or more <a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a> callbacks. If any <b>Add</b> callbacks are issued before the search completes, a <a href="https://msdn.microsoft.com/a125a7b3-6887-42e2-b421-d0e27973d8ee">SearchComplete</a> callback will be issued; otherwise, a <a href="https://msdn.microsoft.com/8f861c69-2967-4a8d-a64a-e2409d722984">SearchFailed</a> callback will be issued.

<i>pszTag</i> is an optional user provided string which will be fed back in either callback, allowing the caller to associate the callback with the original query.

For information about troubleshooting applications calling this method, see <a href="https://msdn.microsoft.com/befe4234-8d3a-4fc5-9a7d-faca94964af6">Troubleshooting WSDAPI Applications</a>.




## -see-also




<a href="https://msdn.microsoft.com/e3d3acc2-914b-40bd-9e1e-a3a612821ab7">IWSDiscoveryProvider</a>
 

 

