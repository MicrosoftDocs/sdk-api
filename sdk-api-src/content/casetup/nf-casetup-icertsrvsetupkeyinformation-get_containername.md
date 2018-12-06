---
UID: NF:casetup.ICertSrvSetupKeyInformation.get_ContainerName
title: ICertSrvSetupKeyInformation::get_ContainerName
author: windows-sdk-content
description: Gets or sets the name used by the cryptographic service provider (CSP) to generate, store, or access the key.
old-location: security\icertsrvsetupkeyinformation_containername.htm
tech.root: seccrypto
ms.assetid: dc644471-6825-48b1-bbfa-da9af6dd0652
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ContainerName property [Security], ContainerName property [Security],ICertSrvSetupKeyInformation interface, ICertSrvSetupKeyInformation interface [Security],ContainerName property, ICertSrvSetupKeyInformation.ContainerName, ICertSrvSetupKeyInformation.get_ContainerName, ICertSrvSetupKeyInformation::ContainerName, ICertSrvSetupKeyInformation::get_ContainerName, ICertSrvSetupKeyInformation::put_ContainerName, casetup/ICertSrvSetupKeyInformation::ContainerName, casetup/ICertSrvSetupKeyInformation::get_ContainerName, casetup/ICertSrvSetupKeyInformation::put_ContainerName, get_ContainerName, security.icertsrvsetupkeyinformation_containername
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
 - ICertSrvSetupKeyInformation.ContainerName
 - ICertSrvSetupKeyInformation.get_ContainerName
 - ICertSrvSetupKeyInformation.put_ContainerName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertSrvSetupKeyInformation::get_ContainerName


## -description


The <b>ContainerName</b> property gets or sets the name used by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) to generate, store, or access the key.

This property is read/write.


## -parameters


## -remarks



If the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> already exists, this name must match the name used by the CSP to access the key.




## -see-also




<a href="https://msdn.microsoft.com/d27c9ba5-ddee-4c9c-b812-e61b974b515a">ICertSrvSetupKeyInformation</a>
 

 

