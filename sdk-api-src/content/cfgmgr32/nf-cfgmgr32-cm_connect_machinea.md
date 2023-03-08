---
UID: NF:cfgmgr32.CM_Connect_MachineA
tech.root: devinst 
title: CM_Connect_MachineA
ms.date: 04/12/2021
targetos: Windows
description: The CM_Connect_Machine function creates a connection to a remote machine. (ANSI)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: cfgmgr32.h
req.idl: 
req.include-header: Cfgmgr32.h 
req.irql: 
req.kmdf-ver: 
req.lib: Cfgmgr32.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows. 
req.target-min-winversvr: 
req.target-type: Desktop
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
api_name:
 - CM_Connect_MachineA
 - CM_Connect_Machine
f1_keywords:
 - CM_Connect_MachineA
 - cfgmgr32/CM_Connect_MachineA
 - CM_Connect_Machine
 - cfgmgr32/CM_Connect_Machine
dev_langs:
 - c++
---


# CM_Connect_MachineA function

## -description

<p class="CCE_Message">[Beginning in Windows 8 and Windows Server 2012 functionality to access remote machines has been removed. You cannot access remote machines when running on these versions of Windows.]

The <b>CM_Connect_Machine</b> function creates a connection to a remote machine.

## -parameters

### -param UNCServerName [in, optional]

Caller-supplied pointer to a text string representing the UNC name, including the <b>\\</b> prefix, of the system for which a connection will be made. If the pointer is <b>NULL</b>, the local system is used.

### -param phMachine [out]

Address of a location to receive a machine handle.

<div class="alert"><b>Note</b> Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

Callers of <b>CM_Connect_Machine</b> must call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_disconnect_machine">CM_Disconnect_Machine</a> to deallocate the machine handle, after it is no longer needed.

Use machine handles obtained with this function only with the <a href="/windows/win32/api/cfgmgr32/">PnP configuration manager functions</a>.

Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_disconnect_machine">CM_Disconnect_Machine</a>
