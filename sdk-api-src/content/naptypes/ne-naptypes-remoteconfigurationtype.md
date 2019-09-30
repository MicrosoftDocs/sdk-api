---
UID: NE:naptypes.tagRemoteConfigurationType
title: RemoteConfigurationType (naptypes.h)
author: windows-sdk-content
description: Describes the type of remote configuration possible for a component.
old-location: nap\remoteconfigurationtype.htm
tech.root: NAP
ms.assetid: 951fbae2-48cb-4e3f-a03f-bf55bf017ec5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RemoteConfigurationType, RemoteConfigurationType enumeration [NAP], nap.remoteconfigurationtype, naptypes/RemoteConfigurationType, naptypes/remoteConfigTypeConfigBlob, naptypes/remoteConfigTypeMachine, remoteConfigTypeConfigBlob, remoteConfigTypeMachine
ms.topic: enum
f1_keywords: 
 - "naptypes/RemoteConfigurationType"
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
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
 - NapTypes.h
api_name:
 - RemoteConfigurationType
targetos: Windows
req.typenames: RemoteConfigurationType
req.redist: 
ms.custom: 19H1
---

# RemoteConfigurationType enumeration


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>RemoteConfigurationType</b> enumeration describes the type of remote configuration possible for a component.


## -enum-fields




### -field remoteConfigTypeMachine

The component allows  remote configuration directly on the machine.


### -field remoteConfigTypeConfigBlob

The component allows remote configuration via a binary large object (BLOB) loaded in memory.

