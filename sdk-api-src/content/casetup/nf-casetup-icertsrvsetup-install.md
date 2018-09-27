---
UID: NF:casetup.ICertSrvSetup.Install
title: ICertSrvSetup::Install
author: windows-sdk-content
description: Installs a role as configured in the CCertSrvSetup object.
old-location: security\icertsrvsetup_install.htm
tech.root: seccrypto
ms.assetid: e07b1cdd-ccb6-4398-862b-521ac1d39f66
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ICertSrvSetup interface [Security],Install method, ICertSrvSetup.Install, ICertSrvSetup::Install, Install, Install method [Security], Install method [Security],ICertSrvSetup interface, casetup/ICertSrvSetup::Install, security.icertsrvsetup_install
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
 - ICertSrvSetup.Install
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertSrvSetup::Install


## -description


The <b>Install</b> method installs a role as configured in the <b>CCertSrvSetup</b> object.


## -parameters






## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/Bb736394(v=VS.85).aspx">InitializeDefaults</a> method must be called before calling this or any other method on a <b>CCertSrvSetup</b> object.

Unless the key already exists, the <b>Install</b> method creates a key for the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) certificate. If the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">cryptographic service provider</a> (CSP) requires interaction, it prompts the user. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb736371(v=VS.85).aspx">ICertSrvSetup</a>
 

 

