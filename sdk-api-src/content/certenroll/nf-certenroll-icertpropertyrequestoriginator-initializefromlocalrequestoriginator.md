---
UID: NF:certenroll.ICertPropertyRequestOriginator.InitializeFromLocalRequestOriginator
title: ICertPropertyRequestOriginator::InitializeFromLocalRequestOriginator
author: windows-sdk-content
description: Initializes the object from the DNS name of the local computer.
old-location: security\icertpropertyrequestoriginator_initializefromlocalrequestoriginator_method.htm
tech.root: SecCertEnroll
ms.assetid: 466e0767-d13a-4f5d-9715-47bb7b9d4142
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ICertPropertyRequestOriginator interface [Security],InitializeFromLocalRequestOriginator method, ICertPropertyRequestOriginator.InitializeFromLocalRequestOriginator, ICertPropertyRequestOriginator::InitializeFromLocalRequestOriginator, InitializeFromLocalRequestOriginator, InitializeFromLocalRequestOriginator method [Security], InitializeFromLocalRequestOriginator method [Security],ICertPropertyRequestOriginator interface, certenroll/ICertPropertyRequestOriginator::InitializeFromLocalRequestOriginator, security.icertpropertyrequestoriginator_initializefromlocalrequestoriginator_method
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
 - ICertPropertyRequestOriginator.InitializeFromLocalRequestOriginator
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
- ICertPropertyRequestOriginator.InitializeFromLocalRequestOriginator
: 
---

# ICertPropertyRequestOriginator::InitializeFromLocalRequestOriginator


## -description


The <b>InitializeFromLocalRequestOriginator</b> method initializes the object from the DNS name of the local computer.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa375928(v=VS.85).aspx">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://msdn.microsoft.com/en-us/library/Aa375789(v=VS.85).aspx">RequestOriginator</a> property to retrieve the DNS name of the originating computer.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375772(v=VS.85).aspx">ICertPropertyRequestOriginator</a>
 

 

