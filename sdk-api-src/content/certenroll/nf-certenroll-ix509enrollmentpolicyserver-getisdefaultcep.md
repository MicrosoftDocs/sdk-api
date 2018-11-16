---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetIsDefaultCEP
title: IX509EnrollmentPolicyServer::GetIsDefaultCEP
author: windows-sdk-content
description: Retrieves a Boolean value that specifies whether this is the default certificate enrollment policy (CEP) server.
old-location: security\ix509enrollmentpolicyserver_getisdefaultcep.htm
tech.root: SecCertEnroll
ms.assetid: 9c84993b-5d08-45c1-8139-458b047028aa
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetIsDefaultCEP, GetIsDefaultCEP method [Security], GetIsDefaultCEP method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetIsDefaultCEP method, IX509EnrollmentPolicyServer.GetIsDefaultCEP, IX509EnrollmentPolicyServer::GetIsDefaultCEP, certenroll/IX509EnrollmentPolicyServer::GetIsDefaultCEP, security.ix509enrollmentpolicyserver_getisdefaultcep
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509EnrollmentPolicyServer.GetIsDefaultCEP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509EnrollmentPolicyServer.GetIsDefaultCEP
: 
---

# IX509EnrollmentPolicyServer::GetIsDefaultCEP


## -description


The <b>GetIsDefaultCEP</b> method retrieves a Boolean value that specifies whether this is the default certificate enrollment policy (CEP) server.


## -parameters




### -param pValue [out, retval]

Pointer to a Boolean value that specifies whether this is the default server.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



The default server is set by the <a href="https://msdn.microsoft.com/en-us/library/Ee351591(v=VS.85).aspx">Initialize</a> method on the <a href="https://msdn.microsoft.com/en-us/library/Ee338624(v=VS.85).aspx">ICertPropertyEnrollmentPolicyServer</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee351692(v=VS.85).aspx">IX509EnrollmentPolicyServer</a>
 

 

