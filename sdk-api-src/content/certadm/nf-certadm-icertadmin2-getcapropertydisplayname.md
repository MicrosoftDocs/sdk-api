---
UID: NF:certadm.ICertAdmin2.GetCAPropertyDisplayName
title: ICertAdmin2::GetCAPropertyDisplayName (certadm.h)
description: The ICertAdmin2::GetCAPropertyDisplayName method retrieves the property display name for a certification authority (CA) property.
helpviewer_keywords: ["CCertAdmin object [Security]","GetCAPropertyDisplayName method","GetCAPropertyDisplayName","GetCAPropertyDisplayName method [Security]","GetCAPropertyDisplayName method [Security]","CCertAdmin object","GetCAPropertyDisplayName method [Security]","ICertAdmin2 interface","ICertAdmin2 interface [Security]","GetCAPropertyDisplayName method","ICertAdmin2.GetCAPropertyDisplayName","ICertAdmin2::GetCAPropertyDisplayName","_certsrv_icertadmin2_getcapropertydisplayname","certadm/ICertAdmin2::GetCAPropertyDisplayName","security.icertadmin2_getcapropertydisplayname"]
old-location: security\icertadmin2_getcapropertydisplayname.htm
tech.root: security
ms.assetid: 8f879b94-d15a-48e6-9e71-a24c1c39c618
ms.date: 12/05/2018
ms.keywords: CCertAdmin object [Security],GetCAPropertyDisplayName method, GetCAPropertyDisplayName, GetCAPropertyDisplayName method [Security], GetCAPropertyDisplayName method [Security],CCertAdmin object, GetCAPropertyDisplayName method [Security],ICertAdmin2 interface, ICertAdmin2 interface [Security],GetCAPropertyDisplayName method, ICertAdmin2.GetCAPropertyDisplayName, ICertAdmin2::GetCAPropertyDisplayName, _certsrv_icertadmin2_getcapropertydisplayname, certadm/ICertAdmin2::GetCAPropertyDisplayName, security.icertadmin2_getcapropertydisplayname
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertAdmin2::GetCAPropertyDisplayName
 - certadm/ICertAdmin2::GetCAPropertyDisplayName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin2.GetCAPropertyDisplayName
 - CCertAdmin.GetCAPropertyDisplayName
---

# ICertAdmin2::GetCAPropertyDisplayName


## -description

The <b>GetCAPropertyDisplayName</b> method retrieves the property display name for a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) property. This method was first defined in the <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a> interface.

## -parameters

### -param strConfig [in]

Represents a valid configuration string for the CA in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>GetCAPropertyDisplayName</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param PropId [in]

Specifies the property identifier. For information about this parameter, see the table in 
<a href="/windows/desktop/api/certadm/nf-certadm-icertadmin2-getcaproperty">ICertAdmin2::GetCAProperty</a>.

### -param pstrDisplayName [out]

A pointer to the string representing the property's display name.

It is the responsibility of the caller to free the <b>BSTR</b> when done by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

## -returns

<h3>C++</h3>
The return value is an <b>HRESULT</b>. A value of S_OK indicates the method was successful.

<h3>VB</h3>
A string that represents the property's display name.