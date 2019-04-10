---
UID: NF:casetup.ICertSrvSetup.SetWebCAInformation
title: ICertSrvSetup::SetWebCAInformation (casetup.h)
author: windows-sdk-content
description: Sets the certification authority (CA) information for the Certification Authority Web Enrollment role.
old-location: security\icertsrvsetup_setwebcainformation.htm
tech.root: SecCrypto
ms.assetid: 6c8d6b06-d36c-496f-8d5a-da20f09a2b0a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICertSrvSetup interface [Security],SetWebCAInformation method, ICertSrvSetup.SetWebCAInformation, ICertSrvSetup::SetWebCAInformation, SetWebCAInformation, SetWebCAInformation method [Security], SetWebCAInformation method [Security],ICertSrvSetup interface, casetup/ICertSrvSetup::SetWebCAInformation, security.icertsrvsetup_setwebcainformation
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
 - ICertSrvSetup.SetWebCAInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertSrvSetup::SetWebCAInformation


## -description


The <b>SetWebCAInformation</b> method sets the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) information for the Certification Authority Web Enrollment role. You can use this method to enable certificate-related requests to a remote CA through a web interface.


## -parameters




### -param bstrCAConfiguration [in]

A string that contains a valid configuration for the CA. The string must be in the form <i>ComputerName</i> or <i>ComputerName\CAName</i>, where <i>ComputerName</i> is the network name of the CA host computer, and <i>CAName</i> is the common name of the CA.


## -remarks



The <b>SetWebCAInformation</b> method pings the CA computer to verify that it is available on the network.

Upon success, <b>SetWebCAInformation</b> sets the ENUM_SETUPPROP_WEBCAMACHINE and ENUM_SETUPPROP_WEBCANAME properties for the Certification Authority Web Enrollment role configuration.
For more information about setup properties, see <a href="https://msdn.microsoft.com/en-us/library/Bb648668(v=VS.85).aspx">CASetupProperty</a>.




## -see-also




<a href="https://msdn.microsoft.com/6792a0d6-d304-481d-a97b-5fb7033c7eae">ICertSrvSetup</a>
 

 

