---
UID: NF:certenroll.ICspInformations.GetCspStatusFromProviderName
title: ICspInformations::GetCspStatusFromProviderName
author: windows-sdk-content
description: Retrieves an ICspStatus object for a legacy provider by provider name and supported key operations.
old-location: security\icspinformations_getcspstatusfromprovidername_method.htm
tech.root: SecCertEnroll
ms.assetid: f73d40cb-dde3-46a5-ba9f-f7cbfa2efe70
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetCspStatusFromProviderName, GetCspStatusFromProviderName method [Security], GetCspStatusFromProviderName method [Security],ICspInformations interface, ICspInformations interface [Security],GetCspStatusFromProviderName method, ICspInformations.GetCspStatusFromProviderName, ICspInformations::GetCspStatusFromProviderName, certenroll/ICspInformations::GetCspStatusFromProviderName, security.icspinformations_getcspstatusfromprovidername_method
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
 - ICspInformations.GetCspStatusFromProviderName
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
- ICspInformations.GetCspStatusFromProviderName
: 
---

# ICspInformations::GetCspStatusFromProviderName


## -description


The <b>GetCspStatusFromProviderName</b> method retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a> object for a legacy provider by provider name and supported key operations. This method is web enabled.


## -parameters




### -param strProviderName [in]

A <b>BSTR</b> that contains the cryptographic provider name or the provider and algorithm names separated by a comma in the format <i>algorithm_name, provider_name</i>.


### -param LegacyKeySpec [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa379409(v=VS.85).aspx">X509KeySpec</a> enumeration value that specifies whether a key can be used for  encryption, signing, or both. This can be one of the following values:

<ul>
<li>XCN_AT_KEYEXCHANGE</li>
<li>XCN_AT_SIGNATURE</li>
</ul>

### -param ppValue [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a> interface that contains information about a cryptographic provider and algorithm pair that satisfies the <i>strProviderName</i> and <i>LegacyKeySpec</i> parameter values.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375968(v=VS.85).aspx">ICspInformations</a>
 

 

