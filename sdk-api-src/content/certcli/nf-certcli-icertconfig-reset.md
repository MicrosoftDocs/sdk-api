---
UID: NF:certcli.ICertConfig.Reset
title: ICertConfig::Reset (certcli.h)
description: Resets the configuration query state to point at the Certificate Services server configuration indexed on the specified configuration point. This method was first defined in the ICertConfig interface.
helpviewer_keywords: ["CCertConfig object [Security]","Reset method","ICertConfig interface [Security]","Reset method","ICertConfig.Reset","ICertConfig2 interface [Security]","Reset method","ICertConfig2::Reset","ICertConfig::Reset","Reset","Reset method [Security]","Reset method [Security]","CCertConfig object","Reset method [Security]","ICertConfig interface","Reset method [Security]","ICertConfig2 interface","_certsrv_icertconfig_reset","certcli/ICertConfig2::Reset","certcli/ICertConfig::Reset","security.icertconfig2_reset"]
old-location: security\icertconfig2_reset.htm
tech.root: security
ms.assetid: 62c24bda-463a-4238-be70-14e28bcbfb39
ms.date: 12/05/2018
ms.keywords: CCertConfig object [Security],Reset method, ICertConfig interface [Security],Reset method, ICertConfig.Reset, ICertConfig2 interface [Security],Reset method, ICertConfig2::Reset, ICertConfig::Reset, Reset, Reset method [Security], Reset method [Security],CCertConfig object, Reset method [Security],ICertConfig interface, Reset method [Security],ICertConfig2 interface, _certsrv_icertconfig_reset, certcli/ICertConfig2::Reset, certcli/ICertConfig::Reset, security.icertconfig2_reset
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
 - ICertConfig::Reset
 - certcli/ICertConfig::Reset
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
 - ICertConfig2.Reset
 - ICertConfig.Reset
 - CCertConfig.Reset
---

# ICertConfig::Reset


## -description

The <b>Reset</b> method resets the configuration query <a href="/windows/desktop/SecGloss/s-gly">state</a> to point at the Certificate Services server configuration indexed on the specified configuration point. This method was first defined in the <a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a> interface.

Each individual configuration indicates a specific Certificate Services server. Some Certificate Services servers may have multiple valid configurations in the configuration database.

## -parameters

### -param Index [in]

Specifies the configuration point used by the configuration query to index a Certificate Services server configuration. The first configuration is index zero.

### -param pCount [out]

A pointer to the number of configurations in the enterprise.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and the <i>pCount</i> parameter points to a <b>Long</b> that contains the number of configurations in the enterprise.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of configurations in the enterprise.

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig2">ICertConfig2</a>



<a href="/windows/desktop/api/certcli/nf-certcli-icertconfig-next">Next</a>