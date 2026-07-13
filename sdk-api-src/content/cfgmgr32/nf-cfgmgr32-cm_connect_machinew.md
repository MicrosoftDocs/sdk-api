---
UID: NF:cfgmgr32.CM_Connect_MachineW
title: CM_Connect_MachineW function (cfgmgr32.h)
description: The CM_Connect_Machine function creates a connection to a remote machine. (Unicode)
helpviewer_keywords: ["CM_Connect_Machine", "CM_Connect_Machine function [Device and Driver Installation]", "CM_Connect_MachineW", "cfgmgr32/CM_Connect_Machine", "cfgmgr32/CM_Connect_MachineW", "cfgmgrfn_5214f459-40fa-4805-b7e4-ee7a1606b659.xml", "devinst.cm_connect_machine"]
old-location: devinst\cm_connect_machine.htm
tech.root: devinst
ms.assetid: 4108a35f-0861-4142-a798-731287515910
ms.date: 12/05/2018
ms.keywords: CM_Connect_Machine, CM_Connect_Machine function [Device and Driver Installation], CM_Connect_MachineW, cfgmgr32/CM_Connect_Machine, cfgmgr32/CM_Connect_MachineW, cfgmgrfn_5214f459-40fa-4805-b7e4-ee7a1606b659.xml, devinst.cm_connect_machine
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Connect_MachineW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Connect_MachineW
 - cfgmgr32/CM_Connect_MachineW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
api_name:
 - CM_Connect_Machine
 - CM_Connect_MachineW
---

# CM_Connect_MachineW function


## -description

<p class="CCE_Message">[Beginning in Windows 8 and Windows Server 2012 functionality to access remote machines has been removed. You cannot access remote machines when running on these versions of Windows.]

The <b>CM_Connect_Machine</b> function creates a connection to a remote machine.

## -parameters

### -param UNCServerName [in, optional]

Caller-supplied pointer to a text string representing the UNC name, including the <b>\\</b> prefix, of the system for which a connection will be made. If the pointer is <b>NULL</b>, the local system is used.

### -param phMachine [out]

Address of a location to receive a machine handle.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

Callers of <b>CM_Connect_Machine</b> must call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_disconnect_machine">CM_Disconnect_Machine</a> to deallocate the machine handle, after it is no longer needed.

Use machine handles obtained with this function only with the <a href="/windows/win32/api/cfgmgr32/">PnP configuration manager functions</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_disconnect_machine">CM_Disconnect_Machine</a>
