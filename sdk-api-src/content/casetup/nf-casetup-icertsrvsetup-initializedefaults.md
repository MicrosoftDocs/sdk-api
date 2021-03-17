---
UID: NF:casetup.ICertSrvSetup.InitializeDefaults
title: ICertSrvSetup::InitializeDefaults (casetup.h)
description: Initializes a CCertSrvSetup object with default values to enable installation of the Certification Authority role.
helpviewer_keywords: ["ICertSrvSetup interface [Security]","InitializeDefaults method","ICertSrvSetup.InitializeDefaults","ICertSrvSetup::InitializeDefaults","InitializeDefaults","InitializeDefaults method [Security]","InitializeDefaults method [Security]","ICertSrvSetup interface","casetup/ICertSrvSetup::InitializeDefaults","security.icertsrvsetup_initializedefaults"]
old-location: security\icertsrvsetup_initializedefaults.htm
tech.root: security
ms.assetid: dff7e2e2-291a-4ea9-858a-8d98d96f79ac
ms.date: 12/05/2018
ms.keywords: ICertSrvSetup interface [Security],InitializeDefaults method, ICertSrvSetup.InitializeDefaults, ICertSrvSetup::InitializeDefaults, InitializeDefaults, InitializeDefaults method [Security], InitializeDefaults method [Security],ICertSrvSetup interface, casetup/ICertSrvSetup::InitializeDefaults, security.icertsrvsetup_initializedefaults
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertSrvSetup::InitializeDefaults
 - casetup/ICertSrvSetup::InitializeDefaults
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetup.InitializeDefaults
---

# ICertSrvSetup::InitializeDefaults


## -description

The <b>InitializeDefaults</b> method initializes a <b>CCertSrvSetup</b> object with default values to enable installation of the Certification Authority role. To install a CA role, this method must be called before using the <b>CCertSrvSetup</b> object. For information about default values, see <a href="/windows/win32/api/casetup/ne-casetup-casetupproperty">CASetupProperty</a>.

## -parameters

### -param bServer [in]

A value that indicates whether a CA will be installed on the computer. A <b>VARIANT_TRUE</b> value indicates that the role will be installed. Neither the Certification Authority nor Certification Authority Web Enrollment roles can be previously installed on the computer.

### -param bClient [in]

A value that indicates whether a Certification Authority Web Enrollment role will be installed on the computer. A <b>VARIANT_TRUE</b> value indicates that the role will be installed. This role cannot be previously installed on the computer.

## -remarks

If the policy statement file "CAPolicy.inf" is installed, <b>InitializeDefaults</b> processes it.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>