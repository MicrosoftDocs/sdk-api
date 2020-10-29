---
UID: NF:certcli.ICertRequest2.GetCAPropertyDisplayName
title: ICertRequest2::GetCAPropertyDisplayName (certcli.h)
description: Retrieves the property display name for a certification authority (CA) property.
helpviewer_keywords: ["CCertRequest object [Security]","GetCAPropertyDisplayName method","GetCAPropertyDisplayName","GetCAPropertyDisplayName method [Security]","GetCAPropertyDisplayName method [Security]","CCertRequest object","GetCAPropertyDisplayName method [Security]","ICertRequest interface","GetCAPropertyDisplayName method [Security]","ICertRequest2 interface","GetCAPropertyDisplayName method [Security]","ICertRequest3 interface","ICertRequest interface [Security]","GetCAPropertyDisplayName method","ICertRequest2 interface [Security]","GetCAPropertyDisplayName method","ICertRequest2.GetCAPropertyDisplayName","ICertRequest2::GetCAPropertyDisplayName","ICertRequest3 interface [Security]","GetCAPropertyDisplayName method","ICertRequest3::GetCAPropertyDisplayName","ICertRequest::GetCAPropertyDisplayName","_certsrv_icertrequest2_getcapropertydisplayname","certcli/ICertRequest2::GetCAPropertyDisplayName","certcli/ICertRequest3::GetCAPropertyDisplayName","certcli/ICertRequest::GetCAPropertyDisplayName","security.icertrequest2_getcapropertydisplayname"]
old-location: security\icertrequest2_getcapropertydisplayname.htm
tech.root: security
ms.assetid: 5c294758-b2aa-497b-8377-6c5987576f82
ms.date: 12/05/2018
ms.keywords: CCertRequest object [Security],GetCAPropertyDisplayName method, GetCAPropertyDisplayName, GetCAPropertyDisplayName method [Security], GetCAPropertyDisplayName method [Security],CCertRequest object, GetCAPropertyDisplayName method [Security],ICertRequest interface, GetCAPropertyDisplayName method [Security],ICertRequest2 interface, GetCAPropertyDisplayName method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetCAPropertyDisplayName method, ICertRequest2 interface [Security],GetCAPropertyDisplayName method, ICertRequest2.GetCAPropertyDisplayName, ICertRequest2::GetCAPropertyDisplayName, ICertRequest3 interface [Security],GetCAPropertyDisplayName method, ICertRequest3::GetCAPropertyDisplayName, ICertRequest::GetCAPropertyDisplayName, _certsrv_icertrequest2_getcapropertydisplayname, certcli/ICertRequest2::GetCAPropertyDisplayName, certcli/ICertRequest3::GetCAPropertyDisplayName, certcli/ICertRequest::GetCAPropertyDisplayName, security.icertrequest2_getcapropertydisplayname
req.header: certcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Certcli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertRequest2::GetCAPropertyDisplayName
 - certcli/ICertRequest2::GetCAPropertyDisplayName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertRequest3.GetCAPropertyDisplayName
 - ICertRequest2.GetCAPropertyDisplayName
 - ICertRequest.GetCAPropertyDisplayName
 - CCertRequest.GetCAPropertyDisplayName
---

# ICertRequest2::GetCAPropertyDisplayName


## -description

The <b>GetCAPropertyDisplayName</b> method retrieves the property display name for a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) property.

## -parameters

### -param strConfig [in]

Represents a valid configuration string for the CA in the form <i>ComputerName</i><b>\\</b><i>CAName</i>, where <i>ComputerName</i> is the network name of the Certificate Services server, and <i>CAName</i> is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

### -param PropId [in]

Specifies the property identifier. For information about this parameter, see the table in 
<a href="/windows/desktop/api/certadm/nf-certadm-icertadmin2-getcaproperty">ICertAdmin2::GetCAProperty</a>.

### -param pstrDisplayName [out, retval]

A pointer to the <b>BSTR</b> that represents the property's display name. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is a <b>String</b> that contains the property's display name.

## -remarks

The <b>GetCAPropertyDisplayName</b> method's functionality is similar to that of the <a href="/windows/desktop/api/certadm/nf-certadm-icertadmin2-getcapropertydisplayname">ICertAdmin2::GetCAPropertyDisplayName</a> method. 

In the ICertAdmin2 method, the CA enforces that the caller has CA read access, which is usually only granted to CA officers and CA administrators.

By contrast, in the ICertRequest2 and ICertRequest3 implementations of the method, the CA does not require any access rights by default.  Only Distributed Component Object Model (DCOM) <a href="/windows/desktop/SecGloss/a-gly">access control lists</a> (ACLs) are enforced; for a domain-joined CA, the DCOM ACLs allow Everyone access to the CAs.  Everyone does not include Anonymous.
The CA's request interface can be locked down by using the registry configuration to enforce that the caller has enroll access.

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">CCertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest3">ICertRequest3</a>