---
UID: NF:certcli.ICertRequest2.GetCAPropertyFlags
title: ICertRequest2::GetCAPropertyFlags (certcli.h)
description: Retrieves the property flags for a certification authority (CA) property.
helpviewer_keywords: ["CCertRequest object [Security]","GetCAPropertyFlags method","GetCAPropertyFlags","GetCAPropertyFlags method [Security]","GetCAPropertyFlags method [Security]","CCertRequest object","GetCAPropertyFlags method [Security]","ICertRequest interface","GetCAPropertyFlags method [Security]","ICertRequest2 interface","GetCAPropertyFlags method [Security]","ICertRequest3 interface","ICertRequest interface [Security]","GetCAPropertyFlags method","ICertRequest2 interface [Security]","GetCAPropertyFlags method","ICertRequest2.GetCAPropertyFlags","ICertRequest2::GetCAPropertyFlags","ICertRequest3 interface [Security]","GetCAPropertyFlags method","ICertRequest3::GetCAPropertyFlags","ICertRequest::GetCAPropertyFlags","_certsrv_icertrequest2_getcapropertyflags","certcli/ICertRequest2::GetCAPropertyFlags","certcli/ICertRequest3::GetCAPropertyFlags","certcli/ICertRequest::GetCAPropertyFlags","security.icertrequest2_getcapropertyflags"]
old-location: security\icertrequest2_getcapropertyflags.htm
tech.root: security
ms.assetid: bdc6ab73-a0b4-44cd-9e46-c453dcb45a41
ms.date: 12/05/2018
ms.keywords: CCertRequest object [Security],GetCAPropertyFlags method, GetCAPropertyFlags, GetCAPropertyFlags method [Security], GetCAPropertyFlags method [Security],CCertRequest object, GetCAPropertyFlags method [Security],ICertRequest interface, GetCAPropertyFlags method [Security],ICertRequest2 interface, GetCAPropertyFlags method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetCAPropertyFlags method, ICertRequest2 interface [Security],GetCAPropertyFlags method, ICertRequest2.GetCAPropertyFlags, ICertRequest2::GetCAPropertyFlags, ICertRequest3 interface [Security],GetCAPropertyFlags method, ICertRequest3::GetCAPropertyFlags, ICertRequest::GetCAPropertyFlags, _certsrv_icertrequest2_getcapropertyflags, certcli/ICertRequest2::GetCAPropertyFlags, certcli/ICertRequest3::GetCAPropertyFlags, certcli/ICertRequest::GetCAPropertyFlags, security.icertrequest2_getcapropertyflags
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
 - ICertRequest2::GetCAPropertyFlags
 - certcli/ICertRequest2::GetCAPropertyFlags
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
 - ICertRequest3.GetCAPropertyFlags
 - ICertRequest2.GetCAPropertyFlags
 - ICertRequest.GetCAPropertyFlags
 - CCertRequest.GetCAPropertyFlags
---

# ICertRequest2::GetCAPropertyFlags


## -description

The <b>GetCAPropertyFlags</b> method retrieves the property flags for a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) property.

## -parameters

### -param strConfig [in]

Represents a valid configuration string for the CA in the form <i>ComputerName</i><b>\\</b><i>CAName</i>, where <i>ComputerName</i> is the network name of the Certificate Services server, and <i>CAName</i> is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

### -param PropId [in]

Specifies the property identifier. For information about this parameter, see the table in 
<a href="/windows/desktop/api/certadm/nf-certadm-icertadmin2-getcaproperty">ICertAdmin2::GetCAProperty</a>.

### -param pPropFlags [out, retval]

A pointer to a <b>LONG</b> value that represents the property flags.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is a <b>Long</b> that represents the property flags.

## -remarks

The <b>GetCAPropertyFlags</b> method's functionality is similar to that of the <a href="/windows/desktop/api/certadm/nf-certadm-icertadmin2-getcapropertyflags">ICertAdmin2::GetCAPropertyFlags</a> method. 

In the ICertAdmin2 method, the CA enforces that the caller has CA read access, which is usually only granted to CA officers and CA administrators.

By contrast, in the ICertRequest2 and ICertRequest3 implementations of the method, the CA does not require any access rights by default.  Only Distributed Component Object Model (DCOM) <a href="/windows/desktop/SecGloss/a-gly">access control lists</a> (ACLs) are enforced; for a domain-joined CA, the DCOM ACLs allow Everyone access to the CAs.  Everyone does not include Anonymous.
The CA's request interface can be locked down by using the registry configuration to enforce that the caller has enroll access.

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">CCertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest3">ICertRequest3</a>