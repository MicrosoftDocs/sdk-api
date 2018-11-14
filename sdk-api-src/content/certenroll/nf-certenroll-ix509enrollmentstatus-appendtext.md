---
UID: NF:certenroll.IX509EnrollmentStatus.AppendText
title: IX509EnrollmentStatus::AppendText
author: windows-sdk-content
description: Appends a string to the status information contained in the Text property.
old-location: security\ix509enrollmentstatus_appendtext_method.htm
tech.root: SecCertEnroll
ms.assetid: aa7c3325-c897-49e3-b38c-ff1efead5f26
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AppendText, AppendText method [Security], AppendText method [Security],IX509EnrollmentStatus interface, IX509EnrollmentStatus interface [Security],AppendText method, IX509EnrollmentStatus.AppendText, IX509EnrollmentStatus::AppendText, certenroll/IX509EnrollmentStatus::AppendText, security.ix509enrollmentstatus_appendtext_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509EnrollmentStatus.AppendText
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
- IX509EnrollmentStatus.AppendText
: 
---

# IX509EnrollmentStatus::AppendText


## -description


The <b>AppendText</b> method appends a string to the status information contained in the <a href="https://msdn.microsoft.com/en-us/library/Aa377845(v=VS.85).aspx">Text</a> property.


## -parameters




### -param strText [in]

A <b>BSTR</b> variable that contains the text to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377818(v=VS.85).aspx">IX509EnrollmentStatus</a>
 

 

