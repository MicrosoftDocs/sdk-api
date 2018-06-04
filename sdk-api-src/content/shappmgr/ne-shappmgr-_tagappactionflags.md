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

# _tagAppActionFlags enumeration


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



