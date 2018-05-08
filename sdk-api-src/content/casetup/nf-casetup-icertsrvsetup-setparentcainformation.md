---
UID: NF:casetup.ICertSrvSetup.SetParentCAInformation
title: ICertSrvSetup::SetParentCAInformation
author: windows-driver-content
description: Sets the parent certification authority (CA) information for a subordinate CA configuration.
old-location: security\icertsrvsetup_setparentcainformation.htm
old-project: SecCrypto
ms.assetid: 73c4782d-579d-48d7-b999-f15a2443bbca
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: ICertSrvSetup interface [Security],SetParentCAInformation method, ICertSrvSetup.SetParentCAInformation, ICertSrvSetup::SetParentCAInformation, SetParentCAInformation, SetParentCAInformation method [Security], SetParentCAInformation method [Security],ICertSrvSetup interface, casetup/ICertSrvSetup::SetParentCAInformation, security.icertsrvsetup_setparentcainformation
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CEPSetupProperty
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certocm.dll
api_name:
-	ICertSrvSetup.SetParentCAInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: Certocm.dll
req.irql: 
---

# ICertSrvSetup::SetParentCAInformation


## -description


The <b>SetParentCAInformation</b> method sets the parent <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) information for a subordinate CA configuration. This facilitates retrieval and installation of the subordinate certificate directly from the parent CA. The parent CA must be a Microsoft CA.


## -parameters




### -param bstrCAConfiguration [in]

A string that contains a valid configuration for the parent CA. The string must be in the form <i>ComputerName</i> or <i>ComputerName\CAName</i>, where <i>ComputerName</i> is the network name of the parent CA host computer, and <i>CAName</i> is the common name of the parent CA.


## -remarks



The <b>SetParentCAInformation</b> method pings the parent CA computer to verify that it is available on the network.

Upon success, <b>SetParentCAInformation</b> sets the ENUM_SETUPPROP_PARENTCAMACHINE and ENUM_SETUPPROP_PARENTCANAME properties for the subordinate CA configuration.
For more information about setup properties, see <a href="https://msdn.microsoft.com/2245ad2f-89ca-4478-91d0-cbd7a0648479">CASetupProperty</a>.




## -see-also




<a href="https://msdn.microsoft.com/6792a0d6-d304-481d-a97b-5fb7033c7eae">ICertSrvSetup</a>
 

 

