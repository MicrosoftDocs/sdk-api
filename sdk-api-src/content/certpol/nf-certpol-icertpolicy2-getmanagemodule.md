---
UID: NF:certpol.ICertPolicy2.GetManageModule
title: ICertPolicy2::GetManageModule (certpol.h)
description: Retrieves the ICertManageModule interface associated with the ICertPolicy2 interface by calling GetManageModule and passing in the address of a pointer to an ICertManageModule.
helpviewer_keywords: ["CCertPolicy object [Security]","GetManageModule method","GetManageModule","GetManageModule method [Security]","GetManageModule method [Security]","CCertPolicy object","GetManageModule method [Security]","ICertPolicy2 interface","ICertPolicy2 interface [Security]","GetManageModule method","ICertPolicy2.GetManageModule","ICertPolicy2::GetManageModule","_certsrv_icertpolicy2_getmanagemodule","certpol/ICertPolicy2::GetManageModule","security.icertpolicy2_getmanagemodule"]
old-location: security\icertpolicy2_getmanagemodule.htm
tech.root: security
ms.assetid: a8d45938-1b89-4576-8705-7a174323e072
ms.date: 12/05/2018
ms.keywords: CCertPolicy object [Security],GetManageModule method, GetManageModule, GetManageModule method [Security], GetManageModule method [Security],CCertPolicy object, GetManageModule method [Security],ICertPolicy2 interface, ICertPolicy2 interface [Security],GetManageModule method, ICertPolicy2.GetManageModule, ICertPolicy2::GetManageModule, _certsrv_icertpolicy2_getmanagemodule, certpol/ICertPolicy2::GetManageModule, security.icertpolicy2_getmanagemodule
req.header: certpol.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertPolicy2::GetManageModule
 - certpol/ICertPolicy2::GetManageModule
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certidl.lib
 - Certidl.dll
api_name:
 - ICertPolicy2.GetManageModule
 - CCertPolicy.GetManageModule
---

# ICertPolicy2::GetManageModule


## -description

The <b>GetManageModule</b> method retrieves the <a href="/windows/desktop/api/certmod/nn-certmod-icertmanagemodule">ICertManageModule</a> interface associated with the <a href="/windows/desktop/api/certpol/nn-certpol-icertpolicy2">ICertPolicy2</a> interface by calling <b>GetManageModule</b> and passing in the address of a pointer to an <b>ICertManageModule</b>.

## -parameters

### -param ppManageModule [out]

Pointer to the <a href="/windows/desktop/api/certmod/nn-certmod-icertmanagemodule">ICertManageModule</a> interface associated with the <a href="/windows/desktop/api/certpol/nn-certpol-icertpolicy2">ICertPolicy2</a> interface.

## -returns

<h3>C++</h3>
 The return value is an <b>HRESULT</b>. A value of S_OK indicates the method was successful.

<h3>VB</h3>
The return value is a <b>Variant</b> containing the <a href="/windows/desktop/api/certmod/nn-certmod-icertmanagemodule">ICertManageModule</a> interface associated with the <a href="/windows/desktop/api/certpol/nn-certpol-icertpolicy2">ICertPolicy2</a> interface.

## -see-also

<b>CCertPolicy</b>



<a href="/windows/desktop/api/certpol/nn-certpol-icertpolicy2">ICertPolicy2</a>