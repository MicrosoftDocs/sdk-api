---
UID: NF:casetup.IMSCEPSetup.GetProviderNameList
title: IMSCEPSetup::GetProviderNameList
author: windows-sdk-content
description: Gets the list of cryptographic service providers (CSPs) that provide asymmetric key signature and exchange algorithms on the computer.
old-location: security\imscepsetup_getprovidernamelist.htm
tech.root: seccrypto
ms.assetid: e2b5bae3-fc85-4277-8ee9-3911dacf3302
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetProviderNameList, GetProviderNameList method [Security], GetProviderNameList method [Security],IMSCEPSetup interface, IMSCEPSetup interface [Security],GetProviderNameList method, IMSCEPSetup.GetProviderNameList, IMSCEPSetup::GetProviderNameList, casetup/IMSCEPSetup::GetProviderNameList, security.imscepsetup_getprovidernamelist
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - IMSCEPSetup.GetProviderNameList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- casetup.h
: 
- IMSCEPSetup.GetProviderNameList
: 
---

# IMSCEPSetup::GetProviderNameList


## -description


The <b>GetProviderNameList</b> method gets the list of <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service providers</a> (CSPs) that provide asymmetric key signature and exchange algorithms on the computer.


## -parameters




### -param bExchange [in]

A value that indicates whether the provider names are for exchange key algorithms. A <b>VARIANT_TRUE</b>  value indicates exchange key providers; otherwise, the providers are for signing keys.


### -param pVal [out]

A pointer to a <b>VARIANT</b>  array of <b>VT_BSTR</b> types, where each string represents the name of a CSP.


## -see-also




<a href="https://msdn.microsoft.com/328c6c04-7ade-4b64-bd8a-4314b6e8dc78">IMSCEPSetup</a>
 

 

