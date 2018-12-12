---
UID: NE:shappmgr._tagAppActionFlags
title: APPACTIONFLAGS
author: windows-sdk-content
description: Specifies application management actions supported by an application publisher. These flags are bitmasks passed to IShellApp::GetPossibleActions.
old-location: shell\APPACTIONFLAGS.htm
tech.root: shell
ms.assetid: edfd9b1e-7f4d-4350-9d2c-71f59ca4f7eb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: APPACTIONFLAGS, APPACTIONFLAGS enumeration [Windows Shell], APPACTION_ADDLATER, APPACTION_CANGETSIZE, APPACTION_INSTALL, APPACTION_MODIFY, APPACTION_MODIFYREMOVE, APPACTION_REPAIR, APPACTION_UNINSTALL, APPACTION_UNSCHEDULE, APPACTION_UPGRADE, inet_APPACTIONFLAGS, shappmgr/APPACTIONFLAGS, shappmgr/APPACTION_ADDLATER, shappmgr/APPACTION_CANGETSIZE, shappmgr/APPACTION_INSTALL, shappmgr/APPACTION_MODIFY, shappmgr/APPACTION_MODIFYREMOVE, shappmgr/APPACTION_REPAIR, shappmgr/APPACTION_UNINSTALL, shappmgr/APPACTION_UNSCHEDULE, shappmgr/APPACTION_UPGRADE, shell.APPACTIONFLAGS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
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
 - Shappmgr.h
api_name:
 - APPACTIONFLAGS
product: Windows
targetos: Windows
req.typenames: APPACTIONFLAGS
req.redist: 
---

# APPACTIONFLAGS enumeration


## -description


Specifies application management actions supported by an application publisher. These flags are bitmasks passed to <a href="https://msdn.microsoft.com/e2cdff59-1339-4d00-9bbc-e34e773da1c2">IShellApp::GetPossibleActions</a>.


## -enum-fields




### -field APPACTION_INSTALL

Indicates that the application can be installed. Published applications always set this bit.


### -field APPACTION_UNINSTALL

Not applicable to published applications.


### -field APPACTION_MODIFY

Not applicable to published applications.


### -field APPACTION_REPAIR

Not applicable to published applications.


### -field APPACTION_UPGRADE

Not applicable to published applications.


### -field APPACTION_CANGETSIZE

Not applicable to published applications.


### -field APPACTION_MODIFYREMOVE

Not applicable to published applications.


### -field APPACTION_ADDLATER

Indicates that the application supports scheduled installation.  If this bit is set, then the Control Panel's Add or Remove Programs application presents the user an <b>Add Later</b> button. If you select <b>Add Later</b>, you are prompted to select the desired time of installation. The <a href="https://msdn.microsoft.com/6d8c5720-b48f-4268-810c-c04b14d20d73">IPublishedApp::Install</a> method is then called with the installation time.


### -field APPACTION_UNSCHEDULE

Obsolete.


## -remarks



The Add or Remove Programs application in Control Panel uses only <b><b>APPACTION_INSTALL</b></b> and <b><b>APPACTION_ADDLATER</b></b> for published applications.



