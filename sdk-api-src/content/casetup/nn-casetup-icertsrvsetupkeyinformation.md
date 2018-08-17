---
UID: NN:casetup.ICertSrvSetupKeyInformation
title: ICertSrvSetupKeyInformation
author: windows-sdk-content
description: Defines a set of private key properties that are used for setup of certification authority (CA) or Microsoft Simple Certificate Enrollment Protocol (SCEP) roles.
old-location: security\icertsrvsetupkeyinformation.htm
old-project: SecCrypto
ms.assetid: d27c9ba5-ddee-4c9c-b812-e61b974b515a
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: ICertSrvSetupKeyInformation, ICertSrvSetupKeyInformation interface [Security], ICertSrvSetupKeyInformation interface [Security],described, casetup/ICertSrvSetupKeyInformation, security.icertsrvsetupkeyinformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ICertSrvSetupKeyInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: Certocm.dll
req.irql: 
---

# ICertSrvSetupKeyInformation interface


## -description


The <b>ICertSrvSetupKeyInformation</b> interface defines a set of <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> properties that are used for setup of <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) or Microsoft <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Simple Certificate Enrollment Protocol</a> (SCEP) roles. The information describes either an existing private key or one that setup generates.

Microsoft provides an implementation of this interface in the <b>CCertSrvSetupKeyInformation</b> class.

In C++, you create an instance of this interface by calling the <b>CoCreateInstance</b> function with the <b>CLSID_CCertSrvSetupKeyInformation</b> class identifier.

