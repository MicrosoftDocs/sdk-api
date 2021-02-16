---
UID: NF:adhoc.IDot11AdHocManager.CreateNetwork
title: IDot11AdHocManager::CreateNetwork (adhoc.h)
description: Creates a wireless ad hoc network.
helpviewer_keywords: ["CreateNetwork","CreateNetwork method [NativeWIFI]","CreateNetwork method [NativeWIFI]","IDot11AdHocManager interface","IDot11AdHocManager interface [NativeWIFI]","CreateNetwork method","IDot11AdHocManager.CreateNetwork","IDot11AdHocManager::CreateNetwork","adhoc/IDot11AdHocManager::CreateNetwork","nwifi.idot11adhocmanager_createnetwork"]
old-location: nwifi\idot11adhocmanager_createnetwork.htm
tech.root: nwifi
ms.assetid: 1d9930b3-7bc4-4015-b096-a21fe01f54f5
ms.date: 12/05/2018
ms.keywords: CreateNetwork, CreateNetwork method [NativeWIFI], CreateNetwork method [NativeWIFI],IDot11AdHocManager interface, IDot11AdHocManager interface [NativeWIFI],CreateNetwork method, IDot11AdHocManager.CreateNetwork, IDot11AdHocManager::CreateNetwork, adhoc/IDot11AdHocManager::CreateNetwork, nwifi.idot11adhocmanager_createnetwork
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDot11AdHocManager::CreateNetwork
 - adhoc/IDot11AdHocManager::CreateNetwork
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocManager.CreateNetwork
---

# IDot11AdHocManager::CreateNetwork


## -description

Creates a wireless ad hoc network. Other clients and hosts can connect to this network.

## -parameters

### -param Name [in]

The friendly name of the network. This string should be limited to 32 characters. The SSID should be used as the friendly name. This name is broadcasted in a beacon.

### -param Password [in]

The password used for machine or user authentication on the network. 

The length of the password string depends on the security settings passed in the <i>pSecurity</i> parameter. The following table shows the password length associated with various security settings.

<table>
<tr>
<th>Security Settings</th>
<th>Password Length</th>
</tr>
<tr>
<td>Open-None</td>
<td>0</td>
</tr>
<tr>
<td>Open-WEP</td>
<td>5 or 13 characters; 10 or 26 hexadecimal digits</td>
</tr>
<tr>
<td>WPA2PSK</td>
<td>8 to 63 characters</td>
</tr>
</table>
 

For the enumerated values that correspond to the security settings pair above, see <a href="/windows/desktop/api/adhoc/ne-adhoc-dot11_adhoc_auth_algorithm">DOT11_ADHOC_AUTH_ALGORITHM</a> and <a href="/windows/desktop/api/adhoc/ne-adhoc-dot11_adhoc_cipher_algorithm">DOT11_ADHOC_CIPHER_ALGORITHM</a>

### -param GeographicalId [in]

The geographical location in which the network will be created. For a list of possible values, see <a href="/windows/desktop/Intl/table-of-geographical-locations">Table of Geographical Locations</a>. 

If the interface is not 802.11d conformant, this value is ignored. That means if <a href="/windows/desktop/api/adhoc/nf-adhoc-idot11adhocinterface-isdot11d">IDot11AdHocInterface::IsDot11d</a> returns <b>FALSE</b>, this value is ignored.

If you are not sure which value to use, set <i>GeographicalId</i> to CTRY_DEFAULT. If you use CTRY_DEFAULT, 802.11d conformance is not enforced.

### -param pInterface [in]

An optional pointer to an <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface">IDot11AdHocInterface</a> that specifies the network interface upon which the new network is created. If this parameter is <b>NULL</b>, the first unused interface is used. If all interfaces are in use, the first enumerated interface is used. In that case, the previous network on the interface is disconnected.

### -param pSecurity [in]

A pointer to an <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings">IDot11AdHocSecuritySettings</a> interface that specifies the security settings used on the network.

### -param pContextGuid [in]

An optional parameter that specifies the GUID of the application that created the network. An application can use this identifier to limit the networks enumerated by <a href="/windows/desktop/api/adhoc/nf-adhoc-idot11adhocmanager-getienumdot11adhocnetworks">GetIEnumDot11AdHocNetworks</a> to networks created by the application. For this filtering to work correctly, all instances of the application on all machines must use the same GUID.

### -param pIAdHoc [out]

A pointer to an <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork">IDot11AdHocNetwork</a> interface that represents the created network.

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
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_EXISTS)</b></dt>
</dl>
</td>
<td width="60%">
A network with the specified <i>Name</i> already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_READY)</b></dt>
</dl>
</td>
<td width="60%">
The <i>pInterface</i> interface reports that its radio is turned off.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_CAPABLE)</b></dt>
</dl>
</td>
<td width="60%">
The  <i>pInterface</i> interface reports that it is not capable of forming an ad hoc network. This condition can occur because the NIC does not support ad hoc networks, or because the NIC does not support the security settings supplied by <i>pSecurity</i>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The <i>pSecurity</i> settings are not supported by the <i>pInterface</i> interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ILL_FORMED_PASSWORD)</b></dt>
</dl>
</td>
<td width="60%">
The <i>Password</i> supplied is invalid. The password supplied may be an invalid length for the security settings supplied by <i>pSecurity</i>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
A wireless network interface card was not found on the machine.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_CURRENT_DOMAIN_NOT_ALLOWED)</b></dt>
</dl>
</td>
<td width="60%">
Group policy or administrative settings prohibit the creation of the network.

</td>
</tr>
</table>

## -remarks

After a successful <b>CreateNetwork</b> call, the network object returned by <i>pIAdHoc</i> is provisioned but not constructed. A subsequent call to <a href="/windows/desktop/api/adhoc/nf-adhoc-idot11adhocmanager-commitcreatednetwork">CommitCreatedNetwork</a> initializes the network. Beacons are not sent until the network is committed. 

There are no clients or hosts connected to the network after a <b>CreateNetwork</b> call. Applications are notified of both successful and failed connection attempts using the <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink">IDot11AdHocManagerNotificationSink</a> interface. For information about registering for notifications on that interface, see <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager">IDot11AdHocManager</a>.

## -see-also

<a href="/windows/desktop/api/adhoc/nf-adhoc-idot11adhocmanager-commitcreatednetwork">CommitCreatedNetwork</a>



<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager">IDot11AdHocManager</a>