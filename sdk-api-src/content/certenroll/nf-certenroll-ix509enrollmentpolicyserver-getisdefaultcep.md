---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetIsDefaultCEP
title: IX509EnrollmentPolicyServer::GetIsDefaultCEP
author: windows-sdk-content
description: Retrieves a Boolean value that specifies whether this is the default certificate enrollment policy (CEP) server.
old-location: security\ix509enrollmentpolicyserver_getisdefaultcep.htm
old-project: SecCertEnroll
ms.assetid: 9c84993b-5d08-45c1-8139-458b047028aa
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetIsDefaultCEP, GetIsDefaultCEP method [Security], GetIsDefaultCEP method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetIsDefaultCEP method, IX509EnrollmentPolicyServer.GetIsDefaultCEP, IX509EnrollmentPolicyServer::GetIsDefaultCEP, certenroll/IX509EnrollmentPolicyServer::GetIsDefaultCEP, security.ix509enrollmentpolicyserver_getisdefaultcep
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509RequestType
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
req.lib: 
req.dll: 
req.irql: 
---

# IX509EnrollmentPolicyServer::GetIsDefaultCEP


## -description


The <b>GetIsDefaultCEP</b> method retrieves a Boolean value that specifies whether this is the default certificate enrollment policy (CEP) server.


## -parameters




### -param pValue [out, retval]

Pointer to a Boolean value that specifies whether this is the default server.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The default server is set by the <a href="https://msdn.microsoft.com/5d54ffb2-4a81-4d52-80db-b8526a52bb53">Initialize</a> method on the <a href="https://msdn.microsoft.com/1af7b178-3226-43c3-bfbe-08738f9ef851">ICertPropertyEnrollmentPolicyServer</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a>
 

 

