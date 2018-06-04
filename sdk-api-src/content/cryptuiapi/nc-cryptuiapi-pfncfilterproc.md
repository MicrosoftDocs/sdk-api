---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



