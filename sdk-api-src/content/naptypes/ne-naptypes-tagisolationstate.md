---
UID: NE:naptypes.tagIsolationState
title: tagIsolationState
author: windows-driver-content
description: Describes the isolation state of a connection.
old-location: nap\isolationstate_enum.htm
old-project: NAP
ms.assetid: 79f81e8e-a105-4cc9-b175-8a364648f3a6
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IsolationState, IsolationState enumeration [NAP], isolationStateInProbation, isolationStateNotRestricted, isolationStateRestrictedAccess, nap.isolationstate_enum, naptypes/IsolationState, naptypes/isolationStateInProbation, naptypes/isolationStateNotRestricted, naptypes/isolationStateRestrictedAccess, tagIsolationState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadMUILibraryW (Unicode) and LoadMUILibraryA (ANSI)
req.idl: NapTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IsolationState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	NapTypes.h
api_name:
-	IsolationState
product: Windows
targetos: Windows
req.lib: Muiload.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagIsolationState enumeration


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>IsolationState</b> enumeration  describes the isolation state of a connection.


## -enum-fields




### -field isolationStateNotRestricted

The connection isolation state is not restricted.


### -field isolationStateInProbation

The connection isolation state is probation.


### -field isolationStateRestrictedAccess

The connection isolation state is restricted access.

