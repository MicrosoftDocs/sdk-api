---
UID: NF:casetup.ICertSrvSetup.PreUnInstall
title: ICertSrvSetup::PreUnInstall (casetup.h)
description: Temporarily saves role-specific state information and then it uninstalls the role.
helpviewer_keywords: ["ICertSrvSetup interface [Security]","PreUnInstall method","ICertSrvSetup.PreUnInstall","ICertSrvSetup::PreUnInstall","PreUnInstall","PreUnInstall method [Security]","PreUnInstall method [Security]","ICertSrvSetup interface","casetup/ICertSrvSetup::PreUnInstall","security.icertsrvsetup_preuninstall"]
old-location: security\icertsrvsetup_preuninstall.htm
tech.root: security
ms.assetid: 2872a7fb-fe96-4ace-b5f4-af88350835ab
ms.date: 12/05/2018
ms.keywords: ICertSrvSetup interface [Security],PreUnInstall method, ICertSrvSetup.PreUnInstall, ICertSrvSetup::PreUnInstall, PreUnInstall, PreUnInstall method [Security], PreUnInstall method [Security],ICertSrvSetup interface, casetup/ICertSrvSetup::PreUnInstall, security.icertsrvsetup_preuninstall
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
 - ICertSrvSetup::PreUnInstall
 - casetup/ICertSrvSetup::PreUnInstall
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
 - ICertSrvSetup.PreUnInstall
---

# ICertSrvSetup::PreUnInstall


## -description

The <b>PreUnInstall</b> method temporarily saves role-specific state information and then it uninstalls the role.

## -parameters

### -param bClientOnly [in]

A value that indicates whether the caller wants to only uninstall the Certification Authority Web Enrollment role. A value of <b>VARIANT_TRUE</b> specifies to only uninstall the Certification Authority Web Enrollment role. This only applies if both the Certification Authority and Certification Authority Web Enrollment roles are installed on the computer.

## -remarks

The <b>PreUnInstall</b> method should be called before performing a role-specific uninstall.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>