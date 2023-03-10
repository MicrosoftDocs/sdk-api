---
UID: NS:wct._WAITCHAIN_NODE_INFO
title: WAITCHAIN_NODE_INFO (wct.h)
description: Represents a node in a wait chain.
helpviewer_keywords: ["*PWAITCHAIN_NODE_INFO","PWAITCHAIN_NODE_INFO","PWAITCHAIN_NODE_INFO structure pointer","WAITCHAIN_NODE_INFO","WAITCHAIN_NODE_INFO structure","WctAlpcType","WctComActivationType","WctComType","WctCriticalSectionType","WctMutexType","WctProcessWaitType","WctSendMessageType","WctStatusAbandoned","WctStatusBlocked","WctStatusError","WctStatusNoAccess","WctStatusNotOwned","WctStatusOwned","WctStatusPidOnly","WctStatusPidOnlyRpcss","WctStatusRunning","WctStatusUnknown","WctThreadType","WctThreadWaitType","WctUnknownType","base.waitchain_node_info","wct/PWAITCHAIN_NODE_INFO","wct/WAITCHAIN_NODE_INFO"]
old-location: base\waitchain_node_info.htm
tech.root: Debug
ms.assetid: 7a333924-79a3-4522-aa5a-4fc60690667d
ms.date: 12/05/2018
ms.keywords: '*PWAITCHAIN_NODE_INFO, PWAITCHAIN_NODE_INFO, PWAITCHAIN_NODE_INFO structure pointer, WAITCHAIN_NODE_INFO, WAITCHAIN_NODE_INFO structure, WctAlpcType, WctComActivationType, WctComType, WctCriticalSectionType, WctMutexType, WctProcessWaitType, WctSendMessageType, WctStatusAbandoned, WctStatusBlocked, WctStatusError, WctStatusNoAccess, WctStatusNotOwned, WctStatusOwned, WctStatusPidOnly, WctStatusPidOnlyRpcss, WctStatusRunning, WctStatusUnknown, WctThreadType, WctThreadWaitType, WctUnknownType, base.waitchain_node_info, wct/PWAITCHAIN_NODE_INFO, wct/WAITCHAIN_NODE_INFO'
req.header: wct.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: WAITCHAIN_NODE_INFO, *PWAITCHAIN_NODE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WAITCHAIN_NODE_INFO
 - wct/_WAITCHAIN_NODE_INFO
 - PWAITCHAIN_NODE_INFO
 - wct/PWAITCHAIN_NODE_INFO
 - WAITCHAIN_NODE_INFO
 - wct/WAITCHAIN_NODE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wct.h
api_name:
 - WAITCHAIN_NODE_INFO
---

# WAITCHAIN_NODE_INFO structure


## -description

Represents a node in a wait chain.

## -struct-fields

### -field ObjectType

The object type. This member is one of the following values from the <b>WCT_OBJECT_TYPE</b> enumeration type.

<a id="WctCriticalSectionType"></a>
<a id="wctcriticalsectiontype"></a>
<a id="WCTCRITICALSECTIONTYPE"></a>


#### WctCriticalSectionType

<a id="WctSendMessageType"></a>
<a id="wctsendmessagetype"></a>
<a id="WCTSENDMESSAGETYPE"></a>


#### WctSendMessageType

<a id="WctMutexType"></a>
<a id="wctmutextype"></a>
<a id="WCTMUTEXTYPE"></a>


#### WctMutexType

<a id="WctAlpcType"></a>
<a id="wctalpctype"></a>
<a id="WCTALPCTYPE"></a>


#### WctAlpcType

<a id="WctComType"></a>
<a id="wctcomtype"></a>
<a id="WCTCOMTYPE"></a>


#### WctComType

<a id="WctThreadWaitType"></a>
<a id="wctthreadwaittype"></a>
<a id="WCTTHREADWAITTYPE"></a>


#### WctThreadWaitType

<a id="WctProcessWaitType"></a>
<a id="wctprocesswaittype"></a>
<a id="WCTPROCESSWAITTYPE"></a>


#### WctProcessWaitType

<a id="WctThreadType"></a>
<a id="wctthreadtype"></a>
<a id="WCTTHREADTYPE"></a>


#### WctThreadType

<a id="WctComActivationType"></a>
<a id="wctcomactivationtype"></a>
<a id="WCTCOMACTIVATIONTYPE"></a>


#### WctComActivationType

<a id="WctUnknownType"></a>
<a id="wctunknowntype"></a>
<a id="WCTUNKNOWNTYPE"></a>


#### WctUnknownType

### -field ObjectStatus

The object status.  This member is one of the following values from the <b>WCT_OBJECT_STATUS</b> enumeration type.

<a id="WctStatusNoAccess"></a>
<a id="wctstatusnoaccess"></a>
<a id="WCTSTATUSNOACCESS"></a>


#### WctStatusNoAccess

<a id="WctStatusRunning"></a>
<a id="wctstatusrunning"></a>
<a id="WCTSTATUSRUNNING"></a>


#### WctStatusRunning

<a id="WctStatusBlocked"></a>
<a id="wctstatusblocked"></a>
<a id="WCTSTATUSBLOCKED"></a>


#### WctStatusBlocked

<a id="WctStatusPidOnly"></a>
<a id="wctstatuspidonly"></a>
<a id="WCTSTATUSPIDONLY"></a>


#### WctStatusPidOnly

<a id="WctStatusPidOnlyRpcss"></a>
<a id="wctstatuspidonlyrpcss"></a>
<a id="WCTSTATUSPIDONLYRPCSS"></a>


#### WctStatusPidOnlyRpcss

<a id="WctStatusOwned"></a>
<a id="wctstatusowned"></a>
<a id="WCTSTATUSOWNED"></a>


#### WctStatusOwned

<a id="WctStatusNotOwned"></a>
<a id="wctstatusnotowned"></a>
<a id="WCTSTATUSNOTOWNED"></a>


#### WctStatusNotOwned

<a id="WctStatusAbandoned"></a>
<a id="wctstatusabandoned"></a>
<a id="WCTSTATUSABANDONED"></a>


#### WctStatusAbandoned

<a id="WctStatusUnknown"></a>
<a id="wctstatusunknown"></a>
<a id="WCTSTATUSUNKNOWN"></a>


#### WctStatusUnknown

<a id="WctStatusError"></a>
<a id="wctstatuserror"></a>
<a id="WCTSTATUSERROR"></a>


#### WctStatusError

### -field LockObject

### -field LockObject.ObjectName

The name of the object. Object names are only available for certain object, such as mutexes. If the object does not have a name, this member is an empty string.

### -field LockObject.Timeout

This member is reserved for future use.

### -field LockObject.Alertable

This member is reserved for future use.

### -field ThreadObject

### -field ThreadObject.ProcessId

The process identifier.

### -field ThreadObject.ThreadId

The thread identifier. For COM and ALPC, this member can be 0.

### -field ThreadObject.WaitTime

The wait time.

### -field ThreadObject.ContextSwitches

The number of context switches.

## -see-also

<a href="/windows/desktop/api/wct/nf-wct-getthreadwaitchain">GetThreadWaitChain</a>



<a href="/windows/desktop/api/wct/nc-wct-pwaitchaincallback">WaitChainCallback</a>