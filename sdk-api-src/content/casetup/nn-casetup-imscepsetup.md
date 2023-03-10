---
UID: NN:casetup.IMSCEPSetup
title: IMSCEPSetup (casetup.h)
description: Defines functionality to install and uninstall a Network Device Enrollment Service (NDES) role on a Certificate Services computer.
helpviewer_keywords: ["IMSCEPSetup","IMSCEPSetup interface [Security]","IMSCEPSetup interface [Security]","described","casetup/IMSCEPSetup","security.imscepsetup"]
old-location: security\imscepsetup.htm
tech.root: security
ms.assetid: 328c6c04-7ade-4b64-bd8a-4314b6e8dc78
ms.date: 12/05/2018
ms.keywords: IMSCEPSetup, IMSCEPSetup interface [Security], IMSCEPSetup interface [Security],described, casetup/IMSCEPSetup, security.imscepsetup
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
 - IMSCEPSetup
 - casetup/IMSCEPSetup
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
 - IMSCEPSetup
---

# IMSCEPSetup interface


## -description

The <b>IMSCEPSetup</b> interface defines functionality to install and uninstall a Network Device Enrollment Service (NDES) role on a Certificate Services computer. Implement this interface to provide a custom setup program for installing and uninstalling this role.

Microsoft provides an implementation of this interface in the <b>CMSCEPSetup</b> class. For installation, you must call <a href="/windows/desktop/api/casetup/nf-casetup-imscepsetup-initializedefaults">InitializeDefaults</a> before accessing any properties or calling any other methods on the <b>CMSCEPSetup</b> object.

In C++, you create an instance of this interface by calling the <b>CoCreateInstance</b> function with the <b>CLSID_CMSCEPSetup</b> class identifier.

## -inheritance

The <b>IMSCEPSetup</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMSCEPSetup</b> also has these types of members:

