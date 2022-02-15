---
UID: NF:certenroll.ICspStatuses.Clear
title: ICspStatuses::Clear (certenroll.h)
description: Removes all ICspStatus objects from the collection.
helpviewer_keywords: ["Clear","Clear method [Security]","Clear method [Security]","ICspStatuses interface","ICspStatuses interface [Security]","Clear method","ICspStatuses.Clear","ICspStatuses::Clear","certenroll/ICspStatuses::Clear","security.icspstatuses_clear_method"]
old-location: security\icspstatuses_clear_method.htm
tech.root: security
ms.assetid: 6a959d88-3ee6-4233-8fc7-23c60b24c14e
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [Security], Clear method [Security],ICspStatuses interface, ICspStatuses interface [Security],Clear method, ICspStatuses.Clear, ICspStatuses::Clear, certenroll/ICspStatuses::Clear, security.icspstatuses_clear_method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICspStatuses::Clear
 - certenroll/ICspStatuses::Clear
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspStatuses.Clear
---

# ICspStatuses::Clear


## -description

The <b>Clear</b> method removes all <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> objects from the collection.



## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a>
