---
UID: NF:certcli.ICertRequest3.GetRefreshPolicy
title: ICertRequest3::GetRefreshPolicy (certcli.h)
description: Returns a value that indicates whether a client's cached certificate enrollment policy is out of date and needs to be refreshed.
helpviewer_keywords: ["CCertRequest object [Security]","GetRefreshPolicy method","GetRefreshPolicy","GetRefreshPolicy method [Security]","GetRefreshPolicy method [Security]","CCertRequest object","GetRefreshPolicy method [Security]","ICertRequest3 class","ICertRequest3 class [Security]","GetRefreshPolicy method","ICertRequest3.GetRefreshPolicy","ICertRequest3::GetRefreshPolicy","certcli/ICertRequest3::GetRefreshPolicy","security.icertrequest3_getrefreshpolicy"]
old-location: security\icertrequest3_getrefreshpolicy.htm
tech.root: security
ms.assetid: 0683b9ad-c3d5-418a-8f05-ae06ad74ef1d
ms.date: 12/05/2018
ms.keywords: CCertRequest object [Security],GetRefreshPolicy method, GetRefreshPolicy, GetRefreshPolicy method [Security], GetRefreshPolicy method [Security],CCertRequest object, GetRefreshPolicy method [Security],ICertRequest3 class, ICertRequest3 class [Security],GetRefreshPolicy method, ICertRequest3.GetRefreshPolicy, ICertRequest3::GetRefreshPolicy, certcli/ICertRequest3::GetRefreshPolicy, security.icertrequest3_getrefreshpolicy
req.header: certcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - ICertRequest3::GetRefreshPolicy
 - certcli/ICertRequest3::GetRefreshPolicy
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
 - ICertRequest3.GetRefreshPolicy
 - CCertRequest.GetRefreshPolicy
---

# ICertRequest3::GetRefreshPolicy


## -description

The <b>GetRefreshPolicy</b> method returns a value that indicates whether a client's cached certificate enrollment policy is out of date and needs to be refreshed.

## -parameters

### -param pValue [out, retval]

A pointer to a <b>VARIANT_BOOL</b> variable to receive the refresh indicator.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is a <b>BOOL</b> that indicates whether the client's policy service is out of date.

## -remarks

The <b>GetRefreshPolicy</b> method returns <b>TRUE</b> only when the enrollment server returns a fault. Before calling the <b>GetRefreshPolicy</b> method you must contact the enrollment server. If a fault is returned, then call  the <b>GetRefreshPolicy</b> method from same instance of <a href="/windows/desktop/api/certcli/nn-certcli-icertrequest3">ICertRequest3</a> to determine whether  the cached policy is out of date and needs to be refreshed.