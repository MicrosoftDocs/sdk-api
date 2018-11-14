---
UID: NF:casetup.ICertSrvSetup.GetKeyLengthList
title: ICertSrvSetup::GetKeyLengthList
author: windows-sdk-content
description: Gets the list of key lengths supported by the specified cryptographic service provider (CSP).
old-location: security\icertsrvsetup_getkeylengthlist.htm
tech.root: seccrypto
ms.assetid: 9360522a-05fd-41ae-95b1-9270a9f4f728
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetKeyLengthList, GetKeyLengthList method [Security], GetKeyLengthList method [Security],ICertSrvSetup interface, ICertSrvSetup interface [Security],GetKeyLengthList method, ICertSrvSetup.GetKeyLengthList, ICertSrvSetup::GetKeyLengthList, casetup/ICertSrvSetup::GetKeyLengthList, security.icertsrvsetup_getkeylengthlist
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - ICertSrvSetup.GetKeyLengthList
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
- ICertSrvSetup.GetKeyLengthList
: 
---

# ICertSrvSetup::GetKeyLengthList


## -description


The <b>GetKeyLengthList</b> method gets the list of <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key lengths</a> supported by the specified <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP). This method does not change the state of the <b>CCertSrvSetup</b> object.


## -parameters




### -param bstrProviderName [in]

A string that contains the name of the provider. For key storage providers, this must be in the form <i>PublicKeyAlgorithmName</i>#<i>KeyStorageProviderName</i> for example "RSA#Microsoft Software Key Storage provider".


### -param pVal [out]

A pointer to a <b>VARIANT</b> array of <b>VT_UI4</b> types that correspond to the key lengths supported by the CSP.


## -see-also




<a href="https://msdn.microsoft.com/6792a0d6-d304-481d-a97b-5fb7033c7eae">ICertSrvSetup</a>
 

 

