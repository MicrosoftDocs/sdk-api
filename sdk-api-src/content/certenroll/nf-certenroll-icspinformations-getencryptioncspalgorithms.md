---
UID: NF:certenroll.ICspInformations.GetEncryptionCspAlgorithms
title: ICspInformations::GetEncryptionCspAlgorithms
author: windows-sdk-content
description: Retrieves the collection of encryption algorithms supported by a provider.
old-location: security\icspinformations_getencryptioncspalgorithms_method.htm
old-project: seccertenroll
ms.assetid: 85d2507c-0d0c-47a3-beb9-62af42b3ca3f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetEncryptionCspAlgorithms, GetEncryptionCspAlgorithms method [Security], GetEncryptionCspAlgorithms method [Security],ICspInformations interface, ICspInformations interface [Security],GetEncryptionCspAlgorithms method, ICspInformations.GetEncryptionCspAlgorithms, ICspInformations::GetEncryptionCspAlgorithms, certenroll/ICspInformations::GetEncryptionCspAlgorithms, security.icspinformations_getencryptioncspalgorithms_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspInformations.GetEncryptionCspAlgorithms
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspInformations::GetEncryptionCspAlgorithms


## -description


The <b>GetEncryptionCspAlgorithms</b> method retrieves the collection of encryption algorithms supported by a provider.


## -parameters




### -param pCspInformation [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> interface that represents the provider. This can be a legacy cryptographic service provider (CSP), a Cryptography API: Next Generation (CNG) provider, or <b>NULL</b>. If you specify <b>NULL</b>, this method returns the collection of all encryption algorithms supported by all CSPs and CNG providers.


### -param ppValue [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/bbf8cff4-b1b2-480e-8c30-eb34166db143">ICspAlgorithms</a> interface that represents the collection.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>



<a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a>
 

 

