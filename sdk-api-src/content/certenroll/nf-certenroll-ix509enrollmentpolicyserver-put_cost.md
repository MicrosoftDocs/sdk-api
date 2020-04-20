---
UID: NF:certenroll.IX509EnrollmentPolicyServer.put_Cost
title: IX509EnrollmentPolicyServer::put_Cost (certenroll.h)
description: Specifies and retrieves an arbitrary cost for contacting the certificate enrollment policy server.helpviewer_keywords: ["Cost property [Security]","Cost property [Security]","IX509EnrollmentPolicyServer interface","IX509EnrollmentPolicyServer interface [Security]","Cost property","IX509EnrollmentPolicyServer.Cost","IX509EnrollmentPolicyServer.put_Cost","IX509EnrollmentPolicyServer::Cost","IX509EnrollmentPolicyServer::get_Cost","IX509EnrollmentPolicyServer::put_Cost","certenroll/IX509EnrollmentPolicyServer::Cost","certenroll/IX509EnrollmentPolicyServer::get_Cost","certenroll/IX509EnrollmentPolicyServer::put_Cost","put_Cost","security.ix509enrollmentpolicyserver_cost"]
old-location: security\ix509enrollmentpolicyserver_cost.htm
tech.root: seccertenroll
ms.assetid: e79bc71f-5f7b-47d7-b45b-1279d27439d2
ms.date: 12/05/2018
ms.keywords: Cost property [Security], Cost property [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],Cost property, IX509EnrollmentPolicyServer.Cost, IX509EnrollmentPolicyServer.put_Cost, IX509EnrollmentPolicyServer::Cost, IX509EnrollmentPolicyServer::get_Cost, IX509EnrollmentPolicyServer::put_Cost, certenroll/IX509EnrollmentPolicyServer::Cost, certenroll/IX509EnrollmentPolicyServer::get_Cost, certenroll/IX509EnrollmentPolicyServer::put_Cost, put_Cost, security.ix509enrollmentpolicyserver_cost
f1_keywords:
- certenroll/IX509EnrollmentPolicyServer.Cost
dev_langs:
- c++
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
- IX509EnrollmentPolicyServer.Cost
- IX509EnrollmentPolicyServer.get_Cost
- IX509EnrollmentPolicyServer.put_Cost
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509EnrollmentPolicyServer::put_Cost


## -description


The <b>Cost</b> property specifies and retrieves an arbitrary  cost for contacting the certificate enrollment policy server.

This property is read/write.


## -parameters


## -remarks



If multiple CEP servers have the same ID value (specified when the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-initialize">Initialize</a> method is called), the server with the lowest cost is contacted first. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a>
 

 

