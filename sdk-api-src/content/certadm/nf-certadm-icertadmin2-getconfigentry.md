---
UID: NF:certadm.ICertAdmin2.GetConfigEntry
title: ICertAdmin2::GetConfigEntry (certadm.h)
description: Retrieves configuration information for a certification authority (CA).
helpviewer_keywords: ["GetConfigEntry","GetConfigEntry method [Security]","GetConfigEntry method [Security]","ICertAdmin2 interface","ICertAdmin2 interface [Security]","GetConfigEntry method","ICertAdmin2.GetConfigEntry","ICertAdmin2::GetConfigEntry","certadm/ICertAdmin2::GetConfigEntry","security.icertadmin2_getconfigentry"]
old-location: security\icertadmin2_getconfigentry.htm
tech.root: security
ms.assetid: 1acb9e06-c9e5-419a-899a-b0ae80fab99e
ms.date: 12/05/2018
ms.keywords: GetConfigEntry, GetConfigEntry method [Security], GetConfigEntry method [Security],ICertAdmin2 interface, ICertAdmin2 interface [Security],GetConfigEntry method, ICertAdmin2.GetConfigEntry, ICertAdmin2::GetConfigEntry, certadm/ICertAdmin2::GetConfigEntry, security.icertadmin2_getconfigentry
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
 - ICertAdmin2::GetConfigEntry
 - certadm/ICertAdmin2::GetConfigEntry
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
 - ICertAdmin2.GetConfigEntry
---

# ICertAdmin2::GetConfigEntry


## -description

The <b>GetConfigEntry</b> method retrieves configuration  information for a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA).

## -parameters

### -param strConfig [in]

String value that represents a valid configuration string for the CA in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>. This parameter can be an empty string, in which case the function retrieves configuration information that is not specific to a CA. This parameter cannot be <b>NULL</b>.

<div class="alert"><b>Important</b>  <b>GetConfigEntry</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param strNodePath [in]

String value that represents the node path for the configuration information. This parameter can be an empty string, in which case the function retrieves configuration information from the path identified by <i>strConfig</i>. This parameter cannot be <b>NULL</b>.

### -param strEntryName [in]

String value that represents the name of the entry whose information is being retrieved. This value can be an empty string, in which case all of the entry names are retrieved. This parameter cannot be <b>NULL</b>.

### -param pvarEntry [out]

A pointer to a <b>VARIANT</b> that receives the requested information.

## -returns

<h3>C++</h3>
If the function is successful, the return value is S_OK.

 
If the function fails, the return value is an <b>HRESULT</b> that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is a <b>Variant</b> that represents the retrieved configuration information.

## -remarks

 The configuration information is stored in the registry under the following path.


<b>HKEY_LOCAL_MACHINE</b>&#92;<b>SYSTEM</b>&#92;<b>CurrentControlSet</b>&#92;<b>Services</b>&#92;<b>CertSvc</b>&#92;<b>Configuration</b>&#92;<i>[CASANITIZEDNAME]</i>&#92;<i>[strNodePath]</i>&#92;<i>[strEntryName]</i></p>Where <i>CASANITIZEDNAME</i> is the <a href="/windows/desktop/SecGloss/s-gly">sanitized name</a> for the CA. For more information about sanitized names, see <a href="/windows/desktop/api/certcli/nf-certcli-icertconfig-getconfig">ICertConfig2::GetConfig</a>.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin2</a>