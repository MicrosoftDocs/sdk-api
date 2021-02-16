---
UID: NF:certenroll.IX509EnrollmentStatus.AppendText
title: IX509EnrollmentStatus::AppendText (certenroll.h)
description: Appends a string to the status information contained in the Text property.
helpviewer_keywords: ["AppendText","AppendText method [Security]","AppendText method [Security]","IX509EnrollmentStatus interface","IX509EnrollmentStatus interface [Security]","AppendText method","IX509EnrollmentStatus.AppendText","IX509EnrollmentStatus::AppendText","certenroll/IX509EnrollmentStatus::AppendText","security.ix509enrollmentstatus_appendtext_method"]
old-location: security\ix509enrollmentstatus_appendtext_method.htm
tech.root: security
ms.assetid: aa7c3325-c897-49e3-b38c-ff1efead5f26
ms.date: 12/05/2018
ms.keywords: AppendText, AppendText method [Security], AppendText method [Security],IX509EnrollmentStatus interface, IX509EnrollmentStatus interface [Security],AppendText method, IX509EnrollmentStatus.AppendText, IX509EnrollmentStatus::AppendText, certenroll/IX509EnrollmentStatus::AppendText, security.ix509enrollmentstatus_appendtext_method
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
 - IX509EnrollmentStatus::AppendText
 - certenroll/IX509EnrollmentStatus::AppendText
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
 - IX509EnrollmentStatus.AppendText
---

# IX509EnrollmentStatus::AppendText


## -description

The <b>AppendText</b> method appends a string to the status information contained in the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_text">Text</a> property.

## -parameters

### -param strText [in]

A <b>BSTR</b> variable that contains the text to add.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentstatus">IX509EnrollmentStatus</a>