---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetIsDefaultCEP
title: IX509EnrollmentPolicyServer::GetIsDefaultCEP (certenroll.h)
description: Retrieves a Boolean value that specifies whether this is the default certificate enrollment policy (CEP) server.
helpviewer_keywords: ["GetIsDefaultCEP","GetIsDefaultCEP method [Security]","GetIsDefaultCEP method [Security]","IX509EnrollmentPolicyServer interface","IX509EnrollmentPolicyServer interface [Security]","GetIsDefaultCEP method","IX509EnrollmentPolicyServer.GetIsDefaultCEP","IX509EnrollmentPolicyServer::GetIsDefaultCEP","certenroll/IX509EnrollmentPolicyServer::GetIsDefaultCEP","security.ix509enrollmentpolicyserver_getisdefaultcep"]
old-location: security\ix509enrollmentpolicyserver_getisdefaultcep.htm
tech.root: security
ms.assetid: 9c84993b-5d08-45c1-8139-458b047028aa
ms.date: 12/05/2018
ms.keywords: GetIsDefaultCEP, GetIsDefaultCEP method [Security], GetIsDefaultCEP method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetIsDefaultCEP method, IX509EnrollmentPolicyServer.GetIsDefaultCEP, IX509EnrollmentPolicyServer::GetIsDefaultCEP, certenroll/IX509EnrollmentPolicyServer::GetIsDefaultCEP, security.ix509enrollmentpolicyserver_getisdefaultcep
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
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
 - IX509EnrollmentPolicyServer::GetIsDefaultCEP
 - certenroll/IX509EnrollmentPolicyServer::GetIsDefaultCEP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509EnrollmentPolicyServer.GetIsDefaultCEP
---

# IX509EnrollmentPolicyServer::GetIsDefaultCEP


## -description

The <b>GetIsDefaultCEP</b> method retrieves a Boolean value that specifies whether this is the default certificate enrollment policy (CEP) server.

## -parameters

### -param pValue [out, retval]

Pointer to a Boolean value that specifies whether this is the default server.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The default server is set by the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollmentpolicyserver-initialize">Initialize</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver">ICertPropertyEnrollmentPolicyServer</a> interface.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a>