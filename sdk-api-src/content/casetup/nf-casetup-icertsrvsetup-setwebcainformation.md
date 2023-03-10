---
UID: NF:casetup.ICertSrvSetup.SetWebCAInformation
title: ICertSrvSetup::SetWebCAInformation (casetup.h)
description: Sets the certification authority (CA) information for the Certification Authority Web Enrollment role.
helpviewer_keywords: ["ICertSrvSetup interface [Security]","SetWebCAInformation method","ICertSrvSetup.SetWebCAInformation","ICertSrvSetup::SetWebCAInformation","SetWebCAInformation","SetWebCAInformation method [Security]","SetWebCAInformation method [Security]","ICertSrvSetup interface","casetup/ICertSrvSetup::SetWebCAInformation","security.icertsrvsetup_setwebcainformation"]
old-location: security\icertsrvsetup_setwebcainformation.htm
tech.root: security
ms.assetid: 6c8d6b06-d36c-496f-8d5a-da20f09a2b0a
ms.date: 12/05/2018
ms.keywords: ICertSrvSetup interface [Security],SetWebCAInformation method, ICertSrvSetup.SetWebCAInformation, ICertSrvSetup::SetWebCAInformation, SetWebCAInformation, SetWebCAInformation method [Security], SetWebCAInformation method [Security],ICertSrvSetup interface, casetup/ICertSrvSetup::SetWebCAInformation, security.icertsrvsetup_setwebcainformation
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
 - ICertSrvSetup::SetWebCAInformation
 - casetup/ICertSrvSetup::SetWebCAInformation
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
 - ICertSrvSetup.SetWebCAInformation
---

# ICertSrvSetup::SetWebCAInformation


## -description

The <b>SetWebCAInformation</b> method sets the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) information for the Certification Authority Web Enrollment role. You can use this method to enable certificate-related requests to a remote CA through a web interface.

## -parameters

### -param bstrCAConfiguration [in]

A string that contains a valid configuration for the CA. The string must be in the form <i>ComputerName</i> or <i>ComputerName\CAName</i>, where <i>ComputerName</i> is the network name of the CA host computer, and <i>CAName</i> is the common name of the CA.

## -remarks

The <b>SetWebCAInformation</b> method pings the CA computer to verify that it is available on the network.

Upon success, <b>SetWebCAInformation</b> sets the ENUM_SETUPPROP_WEBCAMACHINE and ENUM_SETUPPROP_WEBCANAME properties for the Certification Authority Web Enrollment role configuration.
For more information about setup properties, see <a href="/windows/win32/api/casetup/ne-casetup-casetupproperty">CASetupProperty</a>.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>