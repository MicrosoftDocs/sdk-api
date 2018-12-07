---
UID: NN:casetup.ICertSrvSetupKeyInformation
title: ICertSrvSetupKeyInformation
author: windows-sdk-content
description: Defines a set of private key properties that are used for setup of certification authority (CA) or Microsoft Simple Certificate Enrollment Protocol (SCEP) roles.
old-location: security\icertsrvsetupkeyinformation.htm
tech.root: seccrypto
ms.assetid: d27c9ba5-ddee-4c9c-b812-e61b974b515a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICertSrvSetupKeyInformation, ICertSrvSetupKeyInformation interface [Security], ICertSrvSetupKeyInformation interface [Security],described, casetup/ICertSrvSetupKeyInformation, security.icertsrvsetupkeyinformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - ICertSrvSetupKeyInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertSrvSetupKeyInformation interface


## -description


The <b>ICertSrvSetupKeyInformation</b> interface defines a set of <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a> properties that are used for setup of <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) or Microsoft <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">Simple Certificate Enrollment Protocol</a> (SCEP) roles. The information describes either an existing private key or one that setup generates.

Microsoft provides an implementation of this interface in the <b>CCertSrvSetupKeyInformation</b> class.

In C++, you create an instance of this interface by calling the <b>CoCreateInstance</b> function with the <b>CLSID_CCertSrvSetupKeyInformation</b> class identifier.

