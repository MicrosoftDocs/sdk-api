---
UID: NF:certenroll.ICspInformations.GetCspStatusFromProviderName
title: ICspInformations::GetCspStatusFromProviderName
author: windows-sdk-content
description: Retrieves an ICspStatus object for a legacy provider by provider name and supported key operations.
old-location: security\icspinformations_getcspstatusfromprovidername_method.htm
old-project: SecCertEnroll
ms.assetid: f73d40cb-dde3-46a5-ba9f-f7cbfa2efe70
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetCspStatusFromProviderName, GetCspStatusFromProviderName method [Security], GetCspStatusFromProviderName method [Security],ICspInformations interface, ICspInformations interface [Security],GetCspStatusFromProviderName method, ICspInformations.GetCspStatusFromProviderName, ICspInformations::GetCspStatusFromProviderName, certenroll/ICspInformations::GetCspStatusFromProviderName, security.icspinformations_getcspstatusfromprovidername_method
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
 - ICspInformations.GetCspStatusFromProviderName
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspInformations::GetCspStatusFromProviderName


## -description


The <b>GetCspStatusFromProviderName</b> method retrieves an <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> object for a legacy provider by provider name and supported key operations. This method is web enabled.


## -parameters




### -param strProviderName [in]

A <b>BSTR</b> that contains the cryptographic provider name or the provider and algorithm names separated by a comma in the format <i>algorithm_name, provider_name</i>.


### -param LegacyKeySpec [in]

An <a href="https://msdn.microsoft.com/d677d46c-3b36-4081-a6db-123ac1cef84b">X509KeySpec</a> enumeration value that specifies whether a key can be used for  encryption, signing, or both. This can be one of the following values:

<ul>
<li>XCN_AT_KEYEXCHANGE</li>
<li>XCN_AT_SIGNATURE</li>
</ul>

### -param ppValue [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> interface that contains information about a cryptographic provider and algorithm pair that satisfies the <i>strProviderName</i> and <i>LegacyKeySpec</i> parameter values.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>



<a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a>
 

 

