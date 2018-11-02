---
UID: NF:casetup.ICertSrvSetup.GetProviderNameList
title: ICertSrvSetup::GetProviderNameList
author: windows-sdk-content
description: Gets the list of cryptographic service providers (CSPs) that provide asymmetric key signature algorithms on the computer.
old-location: security\icertsrvsetup_getprovidernamelist.htm
tech.root: seccrypto
ms.assetid: a0915981-8023-4ce8-a870-7acc75c574ac
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetProviderNameList, GetProviderNameList method [Security], GetProviderNameList method [Security],ICertSrvSetup interface, ICertSrvSetup interface [Security],GetProviderNameList method, ICertSrvSetup.GetProviderNameList, ICertSrvSetup::GetProviderNameList, casetup/ICertSrvSetup::GetProviderNameList, security.icertsrvsetup_getprovidernamelist
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
 - ICertSrvSetup.GetProviderNameList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertSrvSetup::GetProviderNameList


## -description


The <b>GetProviderNameList</b> method gets the list of <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">cryptographic service providers</a> (CSPs) that provide asymmetric key signature algorithms on the computer. This method does not change the state of the <b>CCertSrvSetup</b> object.


## -parameters




### -param pVal [out]

A pointer to a <b>VARIANT</b> array of <b>VT_BSTR</b> types, where each string represents the name of a CSP.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb736371(v=VS.85).aspx">ICertSrvSetup</a>
 

 

