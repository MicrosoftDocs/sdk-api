---
UID: NF:certenroll.IX509EnrollmentStatus.get_Selected
title: IX509EnrollmentStatus::get_Selected (certenroll.h)
description: Specifies or retrieves a value that indicates whether an item can be used during the enrollment process. (Get)
helpviewer_keywords: ["IX509EnrollmentStatus interface [Security]","Selected property","IX509EnrollmentStatus.Selected","IX509EnrollmentStatus.get_Selected","IX509EnrollmentStatus::Selected","IX509EnrollmentStatus::get_Selected","IX509EnrollmentStatus::put_Selected","Selected property [Security]","Selected property [Security]","IX509EnrollmentStatus interface","certenroll/IX509EnrollmentStatus::Selected","certenroll/IX509EnrollmentStatus::get_Selected","certenroll/IX509EnrollmentStatus::put_Selected","get_Selected","security.ix509enrollmentstatus_selected_property"]
old-location: security\ix509enrollmentstatus_selected_property.htm
tech.root: security
ms.assetid: 9050f394-ccad-4a6e-90bc-53af3a874f91
ms.date: 12/05/2018
ms.keywords: IX509EnrollmentStatus interface [Security],Selected property, IX509EnrollmentStatus.Selected, IX509EnrollmentStatus.get_Selected, IX509EnrollmentStatus::Selected, IX509EnrollmentStatus::get_Selected, IX509EnrollmentStatus::put_Selected, Selected property [Security], Selected property [Security],IX509EnrollmentStatus interface, certenroll/IX509EnrollmentStatus::Selected, certenroll/IX509EnrollmentStatus::get_Selected, certenroll/IX509EnrollmentStatus::put_Selected, get_Selected, security.ix509enrollmentstatus_selected_property
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
 - IX509EnrollmentStatus::get_Selected
 - certenroll/IX509EnrollmentStatus::get_Selected
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
 - IX509EnrollmentStatus.Selected
 - IX509EnrollmentStatus.get_Selected
 - IX509EnrollmentStatus.put_Selected
---

# IX509EnrollmentStatus::get_Selected


## -description

The <b>Selected</b> property specifies or retrieves a value that indicates whether an item can be used during the enrollment process.

This property is read/write.

## -parameters

## -remarks

This property is currently used only to identify which cryptographic provider/algorithm pairs can be used to create a key. For more information, see the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-getcspstatuses">GetCspStatuses</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> interface.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentstatus">IX509EnrollmentStatus</a>
