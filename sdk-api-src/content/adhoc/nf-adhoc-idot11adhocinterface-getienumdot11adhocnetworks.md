---
UID: NF:adhoc.IDot11AdHocInterface.GetIEnumDot11AdHocNetworks
title: IDot11AdHocInterface::GetIEnumDot11AdHocNetworks
author: windows-driver-content
description: Gets the collection of networks associated with this NIC.
old-location: nwifi\idot11adhocinterface_getienumdot11adhocnetworks.htm
old-project: NativeWiFi
ms.assetid: 997acc8d-a4e7-43dc-917d-7a2b69f3c049
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetIEnumDot11AdHocNetworks, GetIEnumDot11AdHocNetworks method [NativeWIFI], GetIEnumDot11AdHocNetworks method [NativeWIFI],IDot11AdHocInterface interface, IDot11AdHocInterface interface [NativeWIFI],GetIEnumDot11AdHocNetworks method, IDot11AdHocInterface.GetIEnumDot11AdHocNetworks, IDot11AdHocInterface::GetIEnumDot11AdHocNetworks, adhoc/IDot11AdHocInterface::GetIEnumDot11AdHocNetworks, nwifi.idot11adhocinterface_getienumdot11adhocnetworks
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
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	adhoc.h
api_name:
-	IDot11AdHocInterface.GetIEnumDot11AdHocNetworks
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDot11AdHocInterface::GetIEnumDot11AdHocNetworks


## -description


Gets the collection of networks associated with this NIC.


## -parameters




### -param pFilterGuid [in]

An optional parameter that specifies the GUID of the application that created the network. An application can use this identifier to limit the networks enumerated to networks created by the application. For this filtering to work correctly, all instances of the application on all machines must use the same GUID.


### -param ppEnum [out]

A pointer to a <a href="https://msdn.microsoft.com/5818e921-86bc-4f96-9ecd-3cb9c9a1a488">IEnumDot11AdHocNetworks</a> interface that contains the enumerated networks.


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




<a href="https://msdn.microsoft.com/a4a73ff8-e24a-4f44-9205-c60699d1c27d">IDot11AdHocInterface</a>
 

 

