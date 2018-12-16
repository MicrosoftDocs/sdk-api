---
UID: NE:naptypes.tagExtendedIsolationState
title: ExtendedIsolationState
author: windows-sdk-content
description: Describes the extended isolation state of a connection.
old-location: nap\extendedisolationstate.htm
tech.root: NAP
ms.assetid: 1466247a-eecf-4912-810a-07cabb9c83da
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ExtendedIsolationState, ExtendedIsolationState enumeration [NAP], extendedIsolationStateInfected, extendedIsolationStateNoData, extendedIsolationStateTransition, extendedIsolationStateUnknown, nap.extendedisolationstate, naptypes/ExtendedIsolationState, naptypes/extendedIsolationStateInfected, naptypes/extendedIsolationStateNoData, naptypes/extendedIsolationStateTransition, naptypes/extendedIsolationStateUnknown
ms.topic: enum
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
 - ExtendedIsolationState
product: Windows
targetos: Windows
req.typenames: ExtendedIsolationState
req.redist: 
---

# ExtendedIsolationState enumeration


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>ExtendedIsolationState</b> enumeration describes the extended isolation state of a connection.


## -enum-fields




### -field extendedIsolationStateNoData

No data is available on the connection isolation state.


### -field extendedIsolationStateTransition

The connection isolation state is "transition".


### -field extendedIsolationStateInfected

The connection isolation state is "infected".


### -field extendedIsolationStateUnknown

The connection isolation state is unknown.

