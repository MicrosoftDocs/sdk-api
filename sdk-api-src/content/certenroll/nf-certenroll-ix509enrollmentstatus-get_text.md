---
UID: NF:certenroll.IX509EnrollmentStatus.get_Text
title: IX509EnrollmentStatus::get_Text (certenroll.h)
description: Specifies or retrieves a string that contains a message associated with the status of the enrollment process. (Get)
helpviewer_keywords: ["IX509EnrollmentStatus interface [Security]","Text property","IX509EnrollmentStatus.Text","IX509EnrollmentStatus.get_Text","IX509EnrollmentStatus::Text","IX509EnrollmentStatus::get_Text","IX509EnrollmentStatus::put_Text","Text property [Security]","Text property [Security]","IX509EnrollmentStatus interface","certenroll/IX509EnrollmentStatus::Text","certenroll/IX509EnrollmentStatus::get_Text","certenroll/IX509EnrollmentStatus::put_Text","get_Text","security.ix509enrollmentstatus_text_property"]
old-location: security\ix509enrollmentstatus_text_property.htm
tech.root: security
ms.assetid: 071c4040-cdcf-4a01-918d-397726a235ed
ms.date: 12/05/2018
ms.keywords: IX509EnrollmentStatus interface [Security],Text property, IX509EnrollmentStatus.Text, IX509EnrollmentStatus.get_Text, IX509EnrollmentStatus::Text, IX509EnrollmentStatus::get_Text, IX509EnrollmentStatus::put_Text, Text property [Security], Text property [Security],IX509EnrollmentStatus interface, certenroll/IX509EnrollmentStatus::Text, certenroll/IX509EnrollmentStatus::get_Text, certenroll/IX509EnrollmentStatus::put_Text, get_Text, security.ix509enrollmentstatus_text_property
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
 - IX509EnrollmentStatus::get_Text
 - certenroll/IX509EnrollmentStatus::get_Text
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
 - IX509EnrollmentStatus.Text
 - IX509EnrollmentStatus.get_Text
 - IX509EnrollmentStatus.put_Text
---

# IX509EnrollmentStatus::get_Text


## -description

The <b>Text</b> property specifies or retrieves a string that contains a message associated with the status of the enrollment process.

This property is read/write.

## -parameters

## -remarks

You can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-appendtext">AppendText</a> method to add information to the message.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentstatus">IX509EnrollmentStatus</a>
