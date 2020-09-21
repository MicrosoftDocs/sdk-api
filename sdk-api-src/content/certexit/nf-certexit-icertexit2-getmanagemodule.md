---
UID: NF:certexit.ICertExit2.GetManageModule
title: ICertExit2::GetManageModule (certexit.h)
description: Retrieves the ICertManageModule interface associated with the ICertExit2 interface by calling GetManageModule and passing in the address of a pointer to an ICertManageModule.
helpviewer_keywords: ["CCertExit object [Security]","GetManageModule method","GetManageModule","GetManageModule method [Security]","GetManageModule method [Security]","CCertExit object","GetManageModule method [Security]","ICertExit2 interface","ICertExit2 interface [Security]","GetManageModule method","ICertExit2.GetManageModule","ICertExit2::GetManageModule","certexit/ICertExit2::GetManageModule","security.icertexit2_getmanagemodule"]
old-location: security\icertexit2_getmanagemodule.htm
tech.root: security
ms.assetid: 7f0c1b63-fd09-43b9-9f88-fab154d94e94
ms.date: 12/05/2018
ms.keywords: CCertExit object [Security],GetManageModule method, GetManageModule, GetManageModule method [Security], GetManageModule method [Security],CCertExit object, GetManageModule method [Security],ICertExit2 interface, ICertExit2 interface [Security],GetManageModule method, ICertExit2.GetManageModule, ICertExit2::GetManageModule, certexit/ICertExit2::GetManageModule, security.icertexit2_getmanagemodule
req.header: certexit.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertExit2::GetManageModule
 - certexit/ICertExit2::GetManageModule
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certexit.h
api_name:
 - ICertExit2.GetManageModule
 - CCertExit.GetManageModule
---

# ICertExit2::GetManageModule


## -description

The <b>GetManageModule</b> method retrieves the <a href="/windows/desktop/api/certmod/nn-certmod-icertmanagemodule">ICertManageModule</a> interface associated with the <a href="/windows/desktop/api/certexit/nn-certexit-icertexit2">ICertExit2</a> interface by calling <b>GetManageModule</b> and passing in the address of a pointer to an <b>ICertManageModule</b>.

## -parameters

### -param ppManageModule [out]

Pointer to the <a href="/windows/desktop/api/certmod/nn-certmod-icertmanagemodule">ICertManageModule</a> interface associated with the <a href="/windows/desktop/api/certexit/nn-certexit-icertexit2">ICertExit2</a> interface.

## -returns

<h3>C++</h3>
 The return value is an <b>HRESULT</b>. A value of S_OK indicates the method was successful.

<h3>VB</h3>
The return value is a <b>Variant</b> containing the <a href="/windows/desktop/api/certmod/nn-certmod-icertmanagemodule">ICertManageModule</a> interface associated with the <a href="/windows/desktop/api/certexit/nn-certexit-icertexit2">ICertExit2</a> interface.