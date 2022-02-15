---
UID: NN:casetup.ICertSrvSetup
title: ICertSrvSetup (casetup.h)
description: Defines functionality to install and uninstall Certification Authority (CA) and Certification Authority Web Enrollment roles on a Certificate Services computer.
helpviewer_keywords: ["ICertSrvSetup","ICertSrvSetup interface [Security]","ICertSrvSetup interface [Security]","described","casetup/ICertSrvSetup","security.icertsrvsetup"]
old-location: security\icertsrvsetup.htm
tech.root: security
ms.assetid: 6792a0d6-d304-481d-a97b-5fb7033c7eae
ms.date: 12/05/2018
ms.keywords: ICertSrvSetup, ICertSrvSetup interface [Security], ICertSrvSetup interface [Security],described, casetup/ICertSrvSetup, security.icertsrvsetup
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
 - ICertSrvSetup
 - casetup/ICertSrvSetup
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
 - ICertSrvSetup
---

# ICertSrvSetup interface


## -description

The <b>ICertSrvSetup</b> interface defines functionality to install and uninstall Certification Authority (CA) and Certification Authority Web Enrollment roles on a <a href="/windows/desktop/SecGloss/c-gly">Certificate Services</a> computer.

Microsoft provides an implementation of this interface in the <b>CCertSrvSetup</b> class. For installation, you must call the <a href="/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-initializedefaults">InitializeDefaults</a> method before accessing any properties or calling any other methods on the <b>CCertSrvSetup</b> object.

In C++, you create an instance of this interface by calling the <b>CoCreateInstance</b> function with the <b>CLSID_CCertSrvSetup</b> class identifier.

<b>Windows Server 2008 Standard:  </b>The following services are not available:<ul>
<li>Online Responder Service</li>
<li>Network Device Enrollment Service</li>
</ul>
In addition, the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) service has limited functionality:

<ul>
<li>V2 templates are not supported; therefore, autoenrollment is not supported.</li>
<li>Delegated enrollment agents are not supported.</li>
<li>Role separation is not supported.</li>
</ul>

## -inheritance

The <b>ICertSrvSetup</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertSrvSetup</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
