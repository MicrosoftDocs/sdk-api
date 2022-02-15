---
UID: NF:casetup.IMSCEPSetup.InitializeDefaults
title: IMSCEPSetup::InitializeDefaults (casetup.h)
description: Initializes a CMSCEPSetup object with default values to enable installation of a Network Device Enrollment Service (NDES) role.
helpviewer_keywords: ["IMSCEPSetup interface [Security]","InitializeDefaults method","IMSCEPSetup.InitializeDefaults","IMSCEPSetup::InitializeDefaults","InitializeDefaults","InitializeDefaults method [Security]","InitializeDefaults method [Security]","IMSCEPSetup interface","casetup/IMSCEPSetup::InitializeDefaults","security.imscepsetup_initializedefaults"]
old-location: security\imscepsetup_initializedefaults.htm
tech.root: security
ms.assetid: 25b1fd48-7b2c-4687-af7e-09efd99038b3
ms.date: 12/05/2018
ms.keywords: IMSCEPSetup interface [Security],InitializeDefaults method, IMSCEPSetup.InitializeDefaults, IMSCEPSetup::InitializeDefaults, InitializeDefaults, InitializeDefaults method [Security], InitializeDefaults method [Security],IMSCEPSetup interface, casetup/IMSCEPSetup::InitializeDefaults, security.imscepsetup_initializedefaults
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSCEPSetup::InitializeDefaults
 - casetup/IMSCEPSetup::InitializeDefaults
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
 - IMSCEPSetup.InitializeDefaults
---

# IMSCEPSetup::InitializeDefaults


## -description

The <b>InitializeDefaults</b> method initializes a <b>CMSCEPSetup</b> object with default values to enable installation of a Network Device Enrollment Service (NDES) role. To install an NDES role, this method must be called before using the <b>CMSCEPSetup</b> object. For information about default values, see <a href="/windows/win32/api/casetup/ne-casetup-mscepsetupproperty">MSCEPSetupProperty</a>.



## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-imscepsetup">IMSCEPSetup</a>
