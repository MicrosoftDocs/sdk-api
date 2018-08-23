---
UID: NF:certenroll.ICspInformations.GetHashAlgorithms
title: ICspInformations::GetHashAlgorithms
author: windows-sdk-content
description: Retrieves the collection of hash algorithms supported by a provider.
old-location: security\icspinformations_gethashalgorithms_method.htm
old-project: seccertenroll
ms.assetid: 647cad18-ed2e-4f3a-92d4-28fcfe60a800
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetHashAlgorithms, GetHashAlgorithms method [Security], GetHashAlgorithms method [Security],ICspInformations interface, ICspInformations interface [Security],GetHashAlgorithms method, ICspInformations.GetHashAlgorithms, ICspInformations::GetHashAlgorithms, certenroll/ICspInformations::GetHashAlgorithms, security.icspinformations_gethashalgorithms_method
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
 - ICspInformations.GetHashAlgorithms
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspInformations::GetHashAlgorithms


## -description


The <b>GetHashAlgorithms</b> method retrieves the collection of hash algorithms supported by a provider.


## -parameters




### -param pCspInformation [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a> interface that represents the provider. This can be a legacy cryptographic service provider (CSP), a Cryptography API: Next Generation (CNG) provider, or <b>NULL</b>. If you specify <b>NULL</b>, this method returns the collection of all hash algorithms supported by all CSPs and CNG providers.


### -param ppValue [out]

Address of a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa376785(v=VS.85).aspx">IObjectIds</a> interface that represents the collection.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375968(v=VS.85).aspx">ICspInformations</a>
 

 

