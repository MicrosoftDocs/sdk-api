---
UID: NF:casetup.ICertSrvSetup.SetParentCAInformation
title: ICertSrvSetup::SetParentCAInformation
author: windows-sdk-content
description: Sets the parent certification authority (CA) information for a subordinate CA configuration.
old-location: security\icertsrvsetup_setparentcainformation.htm
tech.root: seccrypto
ms.assetid: 73c4782d-579d-48d7-b999-f15a2443bbca
ms.author: windowssdkdev
ms.date: 11/08/2018
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
 - ICertSrvSetup.SetParentCAInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertSrvSetup::SetParentCAInformation


## -description


The <b>SetParentCAInformation</b> method sets the parent <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) information for a subordinate CA configuration. This facilitates retrieval and installation of the subordinate certificate directly from the parent CA. The parent CA must be a Microsoft CA.


## -parameters




### -param bstrCAConfiguration [in]

A string that contains a valid configuration for the parent CA. The string must be in the form <i>ComputerName</i> or <i>ComputerName\CAName</i>, where <i>ComputerName</i> is the network name of the parent CA host computer, and <i>CAName</i> is the common name of the parent CA.


## -remarks



The <b>SetParentCAInformation</b> method pings the parent CA computer to verify that it is available on the network.

Upon success, <b>SetParentCAInformation</b> sets the ENUM_SETUPPROP_PARENTCAMACHINE and ENUM_SETUPPROP_PARENTCANAME properties for the subordinate CA configuration.
For more information about setup properties, see <a href="https://msdn.microsoft.com/en-us/library/Bb648668(v=VS.85).aspx">CASetupProperty</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb736371(v=VS.85).aspx">ICertSrvSetup</a>
 

 

