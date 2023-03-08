---
UID: NE:wuapi.tagInstallationImpact
title: InstallationImpact (wuapi.h)
description: Defines the possible levels of impact that can be caused by installing or uninstalling an update.
helpviewer_keywords: ["InstallationImpact","InstallationImpact enumeration [Windows Update Agent]","iiMinor","iiNormal","iiRequiresExclusiveHandling","wua.installationimpact","wuapi/InstallationImpact","wuapi/iiMinor","wuapi/iiNormal","wuapi/iiRequiresExclusiveHandling"]
old-location: wua\installationimpact.htm
tech.root: wua
ms.assetid: 156c5aa2-125f-4ffd-b3eb-4dfed280255b
ms.date: 12/05/2018
ms.keywords: InstallationImpact, InstallationImpact enumeration [Windows Update Agent], iiMinor, iiNormal, iiRequiresExclusiveHandling, wua.installationimpact, wuapi/InstallationImpact, wuapi/iiMinor, wuapi/iiNormal, wuapi/iiRequiresExclusiveHandling
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
targetos: Windows
req.typenames: InstallationImpact
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagInstallationImpact
 - wuapi/tagInstallationImpact
 - InstallationImpact
 - wuapi/InstallationImpact
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - InstallationImpact
---

# InstallationImpact enumeration


## -description

Defines the possible levels of impact that can be caused by installing or uninstalling an update.

## -enum-fields

### -field iiNormal:0

Installing or uninstalling an update results in a level of impact on the target computer that is typical of most updates. Therefore, the update does not qualify for any of the special impact ratings that are defined in this topic.

### -field iiMinor:1

Installing or uninstalling an update results in an insignificant impact on the target computer.

The update must meet strict requirements to qualify for this rating. The requirements include, but are not limited to, the following requirements:

<ul>
<li>It must not perform or require a system restart.</li>
<li>It must not display a user interface.</li>
<li>The installation or uninstallation must succeed even if it affects an application or service that is currently being used.</li>
</ul>
 Updates that qualify for this rating may be eligible for special handling in Windows Update Agent (WUA). For example, they may be eligible for accelerated distribution.

### -field iiRequiresExclusiveHandling:2

This update cannot be installed in the same <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-install">IUpdateInstaller::Install</a> or <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-begininstall">IUpdateInstaller::BeginInstall</a> call as any other update.  If you make an <b>IUpdateInstaller::Install</b> or <b>IUpdateInstaller::BeginInstall</b> call that includes an exclusive update along with one or more other updates, the call will return <b>WU_E_EXCLUSIVE_INSTALL_CONFLICT</b>, and no updates will be installed.
