---
UID: NF:casetup.ICertSrvSetupKeyInformation.put_ContainerName
title: ICertSrvSetupKeyInformation::put_ContainerName
author: windows-sdk-content
description: Gets or sets the name used by the cryptographic service provider (CSP) to generate, store, or access the key.
old-location: security\icertsrvsetupkeyinformation_containername.htm
old-project: SecCrypto
ms.assetid: dc644471-6825-48b1-bbfa-da9af6dd0652
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: ContainerName property [Security], ContainerName property [Security],ICertSrvSetupKeyInformation interface, ICertSrvSetupKeyInformation interface [Security],ContainerName property, ICertSrvSetupKeyInformation.ContainerName, ICertSrvSetupKeyInformation.put_ContainerName, ICertSrvSetupKeyInformation::ContainerName, ICertSrvSetupKeyInformation::get_ContainerName, ICertSrvSetupKeyInformation::put_ContainerName, casetup/ICertSrvSetupKeyInformation::ContainerName, casetup/ICertSrvSetupKeyInformation::get_ContainerName, casetup/ICertSrvSetupKeyInformation::put_ContainerName, put_ContainerName, security.icertsrvsetupkeyinformation_containername
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: casetup.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CEPSetupProperty
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetupKeyInformation.ContainerName
 - ICertSrvSetupKeyInformation.get_ContainerName
 - ICertSrvSetupKeyInformation.put_ContainerName
product: Windows
targetos: Windows
req.lib: 
req.dll: Certocm.dll
req.irql: 
---

# ICertSrvSetupKeyInformation::put_ContainerName


## -description


The <b>ContainerName</b> property gets or sets the name used by the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">cryptographic service provider</a> (CSP) to generate, store, or access the key.

This property is read/write.


## -parameters


## -remarks



If the <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a> already exists, this name must match the name used by the CSP to access the key.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb736372(v=VS.85).aspx">ICertSrvSetupKeyInformation</a>
 

 

