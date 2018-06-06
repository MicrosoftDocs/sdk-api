---
UID: NF:casetup.ICertSrvSetup.InitializeDefaults
title: ICertSrvSetup::InitializeDefaults
author: windows-sdk-content
description: Initializes a CCertSrvSetup object with default values to enable installation of the Certification Authority role.
old-location: security\icertsrvsetup_initializedefaults.htm
old-project: SecCrypto
ms.assetid: dff7e2e2-291a-4ea9-858a-8d98d96f79ac
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: ICertSrvSetup interface [Security],InitializeDefaults method, ICertSrvSetup.InitializeDefaults, ICertSrvSetup::InitializeDefaults, InitializeDefaults, InitializeDefaults method [Security], InitializeDefaults method [Security],ICertSrvSetup interface, casetup/ICertSrvSetup::InitializeDefaults, security.icertsrvsetup_initializedefaults
ms.prod: windows
ms.technology: windows-sdk
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
 - ICertSrvSetup.InitializeDefaults
product: Windows
targetos: Windows
req.lib: 
req.dll: Certocm.dll
req.irql: 
---

# ICertSrvSetup::InitializeDefaults


## -description


The <b>InitializeDefaults</b> method initializes a <b>CCertSrvSetup</b> object with default values to enable installation of the Certification Authority role. To install a CA role, this method must be called before using the <b>CCertSrvSetup</b> object. For information about default values, see <a href="https://msdn.microsoft.com/2245ad2f-89ca-4478-91d0-cbd7a0648479">CASetupProperty</a>.


## -parameters




### -param bServer [in]

A value that indicates whether a CA will be installed on the computer. A <b>VARIANT_TRUE</b> value indicates that the role will be installed. Neither the Certification Authority nor Certification Authority Web Enrollment roles can be previously installed on the computer.


### -param bClient [in]

A value that indicates whether a Certification Authority Web Enrollment role will be installed on the computer. A <b>VARIANT_TRUE</b> value indicates that the role will be installed. This role cannot be previously installed on the computer.


## -remarks



If the policy statement file "CAPolicy.inf" is installed, <b>InitializeDefaults</b> processes it.




## -see-also




<a href="https://msdn.microsoft.com/6792a0d6-d304-481d-a97b-5fb7033c7eae">ICertSrvSetup</a>
 

 

