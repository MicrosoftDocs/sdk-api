---
UID: NF:casetup.IMSCEPSetup.PreUnInstall
title: IMSCEPSetup::PreUnInstall (casetup.h)
description: Removes registry and IIS settings for the Network Device Enrollment Service (NDES) role.
helpviewer_keywords: ["IMSCEPSetup interface [Security]","PreUnInstall method","IMSCEPSetup.PreUnInstall","IMSCEPSetup::PreUnInstall","PreUnInstall","PreUnInstall method [Security]","PreUnInstall method [Security]","IMSCEPSetup interface","casetup/IMSCEPSetup::PreUnInstall","security.imscepsetup_preuninstall"]
old-location: security\imscepsetup_preuninstall.htm
tech.root: security
ms.assetid: 7c9ff619-7c26-4dfb-aeac-fa80a1050cf0
ms.date: 12/05/2018
ms.keywords: IMSCEPSetup interface [Security],PreUnInstall method, IMSCEPSetup.PreUnInstall, IMSCEPSetup::PreUnInstall, PreUnInstall, PreUnInstall method [Security], PreUnInstall method [Security],IMSCEPSetup interface, casetup/IMSCEPSetup::PreUnInstall, security.imscepsetup_preuninstall
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
 - IMSCEPSetup::PreUnInstall
 - casetup/IMSCEPSetup::PreUnInstall
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
 - IMSCEPSetup.PreUnInstall
---

# IMSCEPSetup::PreUnInstall


## -description

The <b>PreUnInstall</b> method removes registry and IIS settings for the Network Device Enrollment Service (NDES) role.



## -remarks

You can use this method to support an uninstall of an NDES role. The role must be already installed on the computer. This method should be called before calling the role-specific component-based servicing (CBS) uninstall process.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-imscepsetup">IMSCEPSetup</a>
