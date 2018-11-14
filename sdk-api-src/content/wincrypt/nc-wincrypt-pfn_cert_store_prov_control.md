---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_CONTROL
title: PFN_CERT_STORE_PROV_CONTROL
author: windows-sdk-content
description: The CertStoreProvControl callback function supports the CertControlStore API. All of the API's parameters are passed straight through to the callback. For details, see CertControlStore.
old-location: security\certstoreprovcontrol.htm
tech.root: seccrypto
ms.assetid: 0725d562-d04c-4fde-97f4-a294290266ee
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CertStoreProvControl, CertStoreProvControl callback function [Security], PFN_CERT_STORE_PROV_CONTROL, PFN_CERT_STORE_PROV_CONTROL callback, _crypto2_certstoreprovcontrol, security.certstoreprovcontrol, wincrypt/CertStoreProvControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: wincrypt.h
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
 - Wincrypt.h
api_name:
 - CertStoreProvControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CERT_STORE_PROV_CONTROL callback function


## -description


The <b>CertStoreProvControl</b> callback function supports the <b>CertControlStore</b> API. All of the API's parameters are passed straight through to the callback. For details, see 
<a href="https://msdn.microsoft.com/04cd9349-50c1-44b4-b080-631a24a80d70">CertControlStore</a>.


## -parameters




### -param hStoreProv [in, out]

<b>HCERTSTOREPROV</b> handle to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> passed from the call to <a href="https://msdn.microsoft.com/04cd9349-50c1-44b4-b080-631a24a80d70">CertControlStore</a>.


### -param dwFlags [in]

Passed from the call to <a href="https://msdn.microsoft.com/04cd9349-50c1-44b4-b080-631a24a80d70">CertControlStore</a>.


### -param dwCtrlType [in]

Control action to be taken. Passed from the call to <a href="https://msdn.microsoft.com/04cd9349-50c1-44b4-b080-631a24a80d70">CertControlStore</a>.


### -param *pvCtrlPara [in, optional]

A pointer to a buffer whose structure and content is determined by the values of <i>dwFlags</i> and <i>dwCtrlType</i>. Passed from the call to <a href="https://msdn.microsoft.com/04cd9349-50c1-44b4-b080-631a24a80d70">CertControlStore</a>.


## -returns



Returns <b>TRUE</b> if the function succeeds or <b>FALSE</b> if it fails.



