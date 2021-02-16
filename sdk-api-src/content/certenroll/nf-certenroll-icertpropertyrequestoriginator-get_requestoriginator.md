---
UID: NF:certenroll.ICertPropertyRequestOriginator.get_RequestOriginator
title: ICertPropertyRequestOriginator::get_RequestOriginator (certenroll.h)
description: Retrieves a string that contains the DNS name of the originating computer.
helpviewer_keywords: ["ICertPropertyRequestOriginator interface [Security]","RequestOriginator property","ICertPropertyRequestOriginator.RequestOriginator","ICertPropertyRequestOriginator.get_RequestOriginator","ICertPropertyRequestOriginator::RequestOriginator","ICertPropertyRequestOriginator::get_RequestOriginator","RequestOriginator property [Security]","RequestOriginator property [Security]","ICertPropertyRequestOriginator interface","certenroll/ICertPropertyRequestOriginator::RequestOriginator","certenroll/ICertPropertyRequestOriginator::get_RequestOriginator","get_RequestOriginator","security.icertpropertyrequestoriginator_requestoriginator_property"]
old-location: security\icertpropertyrequestoriginator_requestoriginator_property.htm
tech.root: security
ms.assetid: 0ac6b8da-9183-4683-a172-a9742b40da64
ms.date: 12/05/2018
ms.keywords: ICertPropertyRequestOriginator interface [Security],RequestOriginator property, ICertPropertyRequestOriginator.RequestOriginator, ICertPropertyRequestOriginator.get_RequestOriginator, ICertPropertyRequestOriginator::RequestOriginator, ICertPropertyRequestOriginator::get_RequestOriginator, RequestOriginator property [Security], RequestOriginator property [Security],ICertPropertyRequestOriginator interface, certenroll/ICertPropertyRequestOriginator::RequestOriginator, certenroll/ICertPropertyRequestOriginator::get_RequestOriginator, get_RequestOriginator, security.icertpropertyrequestoriginator_requestoriginator_property
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
 - ICertPropertyRequestOriginator::get_RequestOriginator
 - certenroll/ICertPropertyRequestOriginator::get_RequestOriginator
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
 - ICertPropertyRequestOriginator.RequestOriginator
 - ICertPropertyRequestOriginator.get_RequestOriginator
---

# ICertPropertyRequestOriginator::get_RequestOriginator


## -description

The <b>RequestOriginator</b> property retrieves a string that contains the DNS name of the originating computer.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyrequestoriginator-initialize">Initialize</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyrequestoriginator-initializefromlocalrequestoriginator">InitializeFromLocalRequestOriginator</a> method to specify a value for the <b>RequestOriginator</b> property.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyrequestoriginator">ICertPropertyRequestOriginator</a>