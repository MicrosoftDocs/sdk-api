---
UID: NF:casetup.ICertSrvSetup.PreUnInstall
title: ICertSrvSetup::PreUnInstall
author: windows-sdk-content
description: Temporarily saves role-specific state information and then it uninstalls the role.
old-location: security\icertsrvsetup_preuninstall.htm
tech.root: seccrypto
ms.assetid: 2872a7fb-fe96-4ace-b5f4-af88350835ab
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ICertSrvSetup interface [Security],PreUnInstall method, ICertSrvSetup.PreUnInstall, ICertSrvSetup::PreUnInstall, PreUnInstall, PreUnInstall method [Security], PreUnInstall method [Security],ICertSrvSetup interface, casetup/ICertSrvSetup::PreUnInstall, security.icertsrvsetup_preuninstall
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
 - ICertSrvSetup.PreUnInstall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/6792a0d6-d304-481d-a97b-5fb7033c7eae">ICertSrvSetup</a>
 

 

