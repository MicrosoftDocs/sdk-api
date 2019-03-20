---
UID: NC:cryptuiapi.PFNCFILTERPROC
title: PFNCFILTERPROC (cryptuiapi.h)
author: windows-sdk-content
description: An application-defined callback function that filters the certificates that appear in the digital signature wizard that are displayed by the CryptUIWizDigitalSign function.
old-location: security\pfncfilterproc.htm
tech.root: SecCrypto
ms.assetid: ced0f35c-7e22-4d19-8352-0bfa37ff1a4b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PFNCFILTERPROC, PFNCFILTERPROC callback, PFNCFILTERPROC callback function [Security], cryptuiapi/PFNCFILTERPROC, security.pfncfilterproc
ms.topic: callback
req.header: cryptuiapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Cryptuiapi.h
api_name:
 - PFNCFILTERPROC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFNCFILTERPROC callback function


## -description


The <b>PFNCFILTERPROC</b> function is an application-defined callback function that filters the certificates that appear in the digital signature wizard that are displayed by the <a href="https://msdn.microsoft.com/1d01523e-d47b-49be-82c8-5e98f97be800">CryptUIWizDigitalSign</a> function.


## -parameters




### -param pCertContext [in]

A pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that contains the certificate to filter.


### -param *pfInitialSelectedCert [in]

A Boolean value that specifies whether  the certificate contained in the <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure pointed to by the <i>pCertContext</i> parameter should be initially selected in the dialog box. This parameter is used only if the filter process returns <b>TRUE</b>.


### -param *pvCallbackData [in]

A pointer to user-defined data.


## -returns



A Boolean value that specifies whether the certificate contained in the <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure pointed to by the <i>pCertContext</i> parameter should be displayed in the digital signature wizard.



