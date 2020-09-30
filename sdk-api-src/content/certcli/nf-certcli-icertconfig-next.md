---
UID: NF:certcli.ICertConfig.Next
title: ICertConfig::Next (certcli.h)
description: Retrieves the index of the next available Certificate Services server configuration in the configuration point. This method was first defined in the ICertConfig interface.
helpviewer_keywords: ["CCertConfig object [Security]","Next method","ICertConfig interface [Security]","Next method","ICertConfig.Next","ICertConfig2 interface [Security]","Next method","ICertConfig2::Next","ICertConfig::Next","Next","Next method [Security]","Next method [Security]","CCertConfig object","Next method [Security]","ICertConfig interface","Next method [Security]","ICertConfig2 interface","_certsrv_icertconfig_next","certcli/ICertConfig2::Next","certcli/ICertConfig::Next","security.icertconfig2_next"]
old-location: security\icertconfig2_next.htm
tech.root: security
ms.assetid: af81c25e-94e7-4c50-9e90-612c034e24b4
ms.date: 12/05/2018
ms.keywords: CCertConfig object [Security],Next method, ICertConfig interface [Security],Next method, ICertConfig.Next, ICertConfig2 interface [Security],Next method, ICertConfig2::Next, ICertConfig::Next, Next, Next method [Security], Next method [Security],CCertConfig object, Next method [Security],ICertConfig interface, Next method [Security],ICertConfig2 interface, _certsrv_icertconfig_next, certcli/ICertConfig2::Next, certcli/ICertConfig::Next, security.icertconfig2_next
req.header: certcli.h
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
req.dll: Certcli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertConfig::Next
 - certcli/ICertConfig::Next
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
 - ICertConfig2.Next
 - ICertConfig.Next
 - CCertConfig.Next
---

# ICertConfig::Next


## -description

The <b>Next</b> method retrieves the index of the next available Certificate Services server configuration in the configuration point. This method was first defined in the <a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a> interface.

## -parameters

### -param pIndex [out]

A pointer to a <b>Long</b> variable that will contain the index of the enumerated configuration, or –1 if there are no more configurations to enumerate.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and the <i>pIndex</i> parameter contains the index of the enumerated configuration.  If there are no more configurations to enumerate, the return value is S_FALSE, and the <i>pIndex</i> parameter points to a value of –1.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 Returns a value that specifies the index of the next available Certificate Services server configuration in the configuration point. If no more configurations are available, the method returns a value of –1.

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig2">ICertConfig2</a>



<a href="/windows/desktop/api/certcli/nf-certcli-icertconfig-reset">Reset</a>