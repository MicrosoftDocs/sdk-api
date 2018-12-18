---
UID: NE:wuapi.tagInstallationImpact
title: InstallationImpact
author: windows-sdk-content
description: Defines the possible levels of impact that can be caused by installing or uninstalling an update.
old-location: wua\installationimpact.htm
tech.root: wua_sdk
ms.assetid: 156c5aa2-125f-4ffd-b3eb-4dfed280255b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: InstallationImpact, InstallationImpact enumeration [Windows Update Agent], iiMinor, iiNormal, iiRequiresExclusiveHandling, wua.installationimpact, wuapi/InstallationImpact, wuapi/iiMinor, wuapi/iiNormal, wuapi/iiRequiresExclusiveHandling
ms.topic: enum
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - InstallationImpact
product: Windows
targetos: Windows
req.typenames: InstallationImpact
req.redist: 
---

# InstallationImpact enumeration


## -description


Defines the possible levels of impact that can be caused by installing or uninstalling an update.


## -enum-fields




### -field iiNormal

Installing or uninstalling an update results in a level of impact on the target computer that is typical of most updates. Therefore, the update does not qualify for any of the special impact ratings that are defined in this topic.


### -field iiMinor

Installing or uninstalling an update results in an insignificant impact on the target computer.

The update must meet strict requirements to qualify for this rating. The requirements include, but are not limited to, the following requirements:

<ul>
<li>It must not perform or require a system restart.</li>
<li>It must not display a user interface.</li>
<li>The installation or uninstallation must succeed even if it affects an application or service that is currently being used.</li>
</ul>
 Updates that qualify for this rating may be eligible for special handling in Windows Update Agent (WUA). For example, they may be eligible for accelerated distribution.


### -field iiRequiresExclusiveHandling

This update cannot be installed in the same <a href="https://msdn.microsoft.com/009fc238-fcc4-4131-b770-9f0d0946e741">IUpdateInstaller::Install</a> or <a href="https://msdn.microsoft.com/756ad613-bc6b-48fb-a079-c192aa98ccfe">IUpdateInstaller::BeginInstall</a> call as any other update.  If you make an <b>IUpdateInstaller::Install</b> or <b>IUpdateInstaller::BeginInstall</b> call that includes an exclusive update along with one or more other updates, the call will return <b>WU_E_EXCLUSIVE_INSTALL_CONFLICT</b>, and no updates will be installed.

