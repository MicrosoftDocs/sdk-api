---
UID: NF:casetup.ICertSrvSetup.Install
title: ICertSrvSetup::Install (casetup.h)
description: Installs a role as configured in the CCertSrvSetup object.
helpviewer_keywords: ["ICertSrvSetup interface [Security]","Install method","ICertSrvSetup.Install","ICertSrvSetup::Install","Install","Install method [Security]","Install method [Security]","ICertSrvSetup interface","casetup/ICertSrvSetup::Install","security.icertsrvsetup_install"]
old-location: security\icertsrvsetup_install.htm
tech.root: security
ms.assetid: e07b1cdd-ccb6-4398-862b-521ac1d39f66
ms.date: 12/05/2018
ms.keywords: ICertSrvSetup interface [Security],Install method, ICertSrvSetup.Install, ICertSrvSetup::Install, Install, Install method [Security], Install method [Security],ICertSrvSetup interface, casetup/ICertSrvSetup::Install, security.icertsrvsetup_install
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
 - ICertSrvSetup::Install
 - casetup/ICertSrvSetup::Install
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
 - ICertSrvSetup.Install
---

# ICertSrvSetup::Install


## -description

The <b>Install</b> method installs a role as configured in the <b>CCertSrvSetup</b> object.



## -remarks

The <a href="/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-initializedefaults">InitializeDefaults</a> method must be called before calling this or any other method on a <b>CCertSrvSetup</b> object.

Unless the key already exists, the <b>Install</b> method creates a key for the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) certificate. If the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) requires interaction, it prompts the user.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>
