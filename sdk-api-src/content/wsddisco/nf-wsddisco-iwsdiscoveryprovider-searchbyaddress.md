---
UID: NF:wsddisco.IWSDiscoveryProvider.SearchByAddress
title: IWSDiscoveryProvider::SearchByAddress
author: windows-sdk-content
description: Initializes a search for WS-Discovery hosts by device address.
old-location: ncd\iwsdiscoveryprovider_searchbyaddress.htm
old-project: wsdapi
ms.assetid: 64493841-0715-4bae-a416-aca9945b2420
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWSDiscoveryProvider interface,SearchByAddress method, IWSDiscoveryProvider.SearchByAddress, IWSDiscoveryProvider::SearchByAddress, SearchByAddress, SearchByAddress method, SearchByAddress method,IWSDiscoveryProvider interface, ncd.iwsdiscoveryprovider_searchbyaddress, wsddisco/IWSDiscoveryProvider::SearchByAddress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.redist: 
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
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDiscoveryProvider.SearchByAddress
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDiscoveryProvider::SearchByAddress


## -description


Initializes a search for <a href="http://go.microsoft.com/fwlink/p/?linkid=87841">WS-Discovery</a> hosts by device address.


## -parameters




### -param pszAddress [in]

The HTTP transport address of the device.


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
<i>pszAddress</i> is <b>NULL</b>, the length in characters of <i>pszAddress</i>  exceeds WSD_MAX_TEXT_LENGTH (8192), or the length in characters of  <i>pszTag</i> exceeds WSD_MAX_TEXT_LENGTH (8192).

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



<b>SearchByAddress</b> initiates a WS-Discovery <a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe</a> over HTTP in an attempt to identify a device at a known URL. The Probe is sent to the address specified by <i>pszAddress</i>. This call may result in one or more <a href="https://msdn.microsoft.com/4e36157f-444d-4e59-bc30-c6def9c51cea">Add</a> callbacks. If any <b>Add</b> callbacks are issued before the search completes, a <a href="https://msdn.microsoft.com/a125a7b3-6887-42e2-b421-d0e27973d8ee">SearchComplete</a> callback will be issued; otherwise, a <a href="https://msdn.microsoft.com/8f861c69-2967-4a8d-a64a-e2409d722984">SearchFailed</a> callback will be issued.  The interval between initiating the search and receiving either of these notifications can be up to 30 seconds.

<i>pszTag</i> is an optional user provided string which will be fed back in either callback, allowing the caller to associate the callback with the original query.

For information about troubleshooting applications calling this method, see <a href="https://msdn.microsoft.com/befe4234-8d3a-4fc5-9a7d-faca94964af6">Troubleshooting WSDAPI Applications</a>.




## -see-also




<a href="https://msdn.microsoft.com/e3d3acc2-914b-40bd-9e1e-a3a612821ab7">IWSDiscoveryProvider</a>
 

 

