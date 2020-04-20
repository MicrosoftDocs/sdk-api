---
UID: NF:adhoc.IDot11AdHocManager.GetIEnumDot11AdHocNetworks
title: IDot11AdHocManager::GetIEnumDot11AdHocNetworks (adhoc.h)
description: Returns a list of available ad hoc network destinations within connection range.helpviewer_keywords: ["GetIEnumDot11AdHocNetworks","GetIEnumDot11AdHocNetworks method [NativeWIFI]","GetIEnumDot11AdHocNetworks method [NativeWIFI]","IDot11AdHocManager interface","IDot11AdHocManager interface [NativeWIFI]","GetIEnumDot11AdHocNetworks method","IDot11AdHocManager.GetIEnumDot11AdHocNetworks","IDot11AdHocManager::GetIEnumDot11AdHocNetworks","adhoc/IDot11AdHocManager::GetIEnumDot11AdHocNetworks","nwifi.idot11adhocmanager_getienumdot11adhocnetworks"]
old-location: nwifi\idot11adhocmanager_getienumdot11adhocnetworks.htm
tech.root: NativeWiFi
ms.assetid: 3d37fad8-18e8-4280-9fa8-e40c742ec8ba
ms.date: 12/05/2018
ms.keywords: GetIEnumDot11AdHocNetworks, GetIEnumDot11AdHocNetworks method [NativeWIFI], GetIEnumDot11AdHocNetworks method [NativeWIFI],IDot11AdHocManager interface, IDot11AdHocManager interface [NativeWIFI],GetIEnumDot11AdHocNetworks method, IDot11AdHocManager.GetIEnumDot11AdHocNetworks, IDot11AdHocManager::GetIEnumDot11AdHocNetworks, adhoc/IDot11AdHocManager::GetIEnumDot11AdHocNetworks, nwifi.idot11adhocmanager_getienumdot11adhocnetworks
f1_keywords:
- adhoc/IDot11AdHocManager.GetIEnumDot11AdHocNetworks
dev_langs:
- c++
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
- IDot11AdHocManager.GetIEnumDot11AdHocNetworks
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDot11AdHocManager::GetIEnumDot11AdHocNetworks


## -description


Returns a list of available ad hoc network destinations within connection range. This list may be filtered.


## -parameters




### -param pContextGuid [in]

An optional parameter that specifies the GUID of the application that created the network. An application can use this identifier to limit the networks enumerated to networks created by the application. For this filtering to work correctly, all instances of the application on all machines must use the same GUID.


### -param ppEnum [out]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks">IEnumDot11AdHocNetworks</a> interface that contains the enumerated networks.


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




<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager">IDot11AdHocManager</a>
 

 

