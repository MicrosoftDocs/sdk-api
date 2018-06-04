---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tagInstallationImpact enumeration


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

