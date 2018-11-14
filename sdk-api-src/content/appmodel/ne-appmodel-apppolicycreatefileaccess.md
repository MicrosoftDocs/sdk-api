---
UID: NE:appmodel.AppPolicyCreateFileAccess
title: AppPolicyCreateFileAccess
author: windows-sdk-content
description: The AppPolicyCreateFileAccess enumeration indicates whether a process has full or restricted access to the IO devices (file, file stream, directory, physical disk, volume, console buffer, tape drive, communications resource, mailslot, and pipe).
old-location: appxpkg\apppolicycreatefileaccess_enumeration.htm
tech.root: appxpkg
ms.assetid: B21CF29E-D3B8-46A3-8443-161646E23ECA
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: AppPolicyCreateFileAccess, AppPolicyCreateFileAccess enumeration [App packaging and management], AppPolicyCreateFileAccess_Full, AppPolicyCreateFileAccess_Limited, appmodel/AppPolicyCreateFileAccess, appmodel/AppPolicyCreateFileAccess_Full, appmodel/AppPolicyCreateFileAccess_Limited, appxpkg.apppolicycreatefileaccess_enumeration
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: appmodel.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AppModel.h
api_name:
 - AppPolicyCreateFileAccess
product: Windows
targetos: Windows
req.typenames: AppPolicyCreateFileAccess
req.redist: 
---

# AppPolicyCreateFileAccess enumeration


## -description


The AppPolicyCreateFileAccess enumeration indicates whether a process has full or restricted access to the IO devices (file, file stream, directory, physical disk, volume, console buffer, tape drive, communications resource, mailslot, and pipe).


## -enum-fields




### -field AppPolicyCreateFileAccess_Full

Indicates that the process has full access to the IO devices. This value is expected for a desktop application, or for a Desktop Bridge application.


### -field AppPolicyCreateFileAccess_Limited

Indicates that the process has limited access to the IO devices. This value is expected for a UWP app.

