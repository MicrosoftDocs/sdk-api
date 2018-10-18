---
UID: NF:casetup.IMSCEPSetup.PreUnInstall
title: IMSCEPSetup::PreUnInstall
author: windows-sdk-content
description: Removes registry and IIS settings for the Network Device Enrollment Service (NDES) role.
old-location: security\imscepsetup_preuninstall.htm
tech.root: seccrypto
ms.assetid: 7c9ff619-7c26-4dfb-aeac-fa80a1050cf0
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IMSCEPSetup interface [Security],PreUnInstall method, IMSCEPSetup.PreUnInstall, IMSCEPSetup::PreUnInstall, PreUnInstall, PreUnInstall method [Security], PreUnInstall method [Security],IMSCEPSetup interface, casetup/IMSCEPSetup::PreUnInstall, security.imscepsetup_preuninstall
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - IMSCEPSetup.PreUnInstall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSCEPSetup::PreUnInstall


## -description


The <b>PreUnInstall</b> method removes registry and IIS settings for the Network Device Enrollment Service (NDES) role.


## -parameters






## -remarks



You can use this method to support an uninstall of an NDES role. The role must be already installed on the computer. This method should be called before calling the role-specific component-based servicing (CBS) uninstall process.




## -see-also




<a href="https://msdn.microsoft.com/328c6c04-7ade-4b64-bd8a-4314b6e8dc78">IMSCEPSetup</a>
 

 

