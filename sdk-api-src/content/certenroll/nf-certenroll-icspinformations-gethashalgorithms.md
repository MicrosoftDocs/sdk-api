---
UID: NF:certenroll.ICspInformations.GetHashAlgorithms
title: ICspInformations::GetHashAlgorithms
author: windows-sdk-content
description: Retrieves the collection of hash algorithms supported by a provider.
old-location: security\icspinformations_gethashalgorithms_method.htm
tech.root: seccertenroll
ms.assetid: 647cad18-ed2e-4f3a-92d4-28fcfe60a800
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: GetHashAlgorithms, GetHashAlgorithms method [Security], GetHashAlgorithms method [Security],ICspInformations interface, ICspInformations interface [Security],GetHashAlgorithms method, ICspInformations.GetHashAlgorithms, ICspInformations::GetHashAlgorithms, certenroll/ICspInformations::GetHashAlgorithms, security.icspinformations_gethashalgorithms_method
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
 - ICspInformations.GetHashAlgorithms
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICspInformations::GetHashAlgorithms


## -description


The <b>GetHashAlgorithms</b> method retrieves the collection of hash algorithms supported by a provider.


## -parameters




### -param pCspInformation [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> interface that represents the provider. This can be a legacy cryptographic service provider (CSP), a Cryptography API: Next Generation (CNG) provider, or <b>NULL</b>. If you specify <b>NULL</b>, this method returns the collection of all hash algorithms supported by all CSPs and CNG providers.


### -param ppValue [out]

Address of a pointer to an <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> interface that represents the collection.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>



<a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a>
 

 

