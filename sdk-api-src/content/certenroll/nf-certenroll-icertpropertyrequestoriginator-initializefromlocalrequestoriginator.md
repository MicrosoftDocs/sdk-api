---
UID: NF:certenroll.ICertPropertyRequestOriginator.InitializeFromLocalRequestOriginator
title: ICertPropertyRequestOriginator::InitializeFromLocalRequestOriginator (certenroll.h)
author: windows-sdk-content
description: Initializes the object from the DNS name of the local computer.
old-location: security\icertpropertyrequestoriginator_initializefromlocalrequestoriginator_method.htm
tech.root: seccertenroll
ms.assetid: 466e0767-d13a-4f5d-9715-47bb7b9d4142
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICertPropertyRequestOriginator interface [Security],InitializeFromLocalRequestOriginator method, ICertPropertyRequestOriginator.InitializeFromLocalRequestOriginator, ICertPropertyRequestOriginator::InitializeFromLocalRequestOriginator, InitializeFromLocalRequestOriginator, InitializeFromLocalRequestOriginator method [Security], InitializeFromLocalRequestOriginator method [Security],ICertPropertyRequestOriginator interface, certenroll/ICertPropertyRequestOriginator::InitializeFromLocalRequestOriginator, security.icertpropertyrequestoriginator_initializefromlocalrequestoriginator_method
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
ms.custom: 19H1
---

# ICertPropertyRequestOriginator::InitializeFromLocalRequestOriginator


## -description


The <b>InitializeFromLocalRequestOriginator</b> method initializes the object from the DNS name of the local computer.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Call the <a href="https://msdn.microsoft.com/46c409c4-46bd-4349-8363-1983f4411bc2">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://msdn.microsoft.com/0ac6b8da-9183-4683-a172-a9742b40da64">RequestOriginator</a> property to retrieve the DNS name of the originating computer.




## -see-also




<a href="https://msdn.microsoft.com/ce33605e-c3ae-4b96-a13e-6f06e8d5ffee">ICertPropertyRequestOriginator</a>
 

 

