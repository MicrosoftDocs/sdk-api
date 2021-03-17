---
UID: NF:cfgmgr32.CM_Disconnect_Machine
title: CM_Disconnect_Machine function (cfgmgr32.h)
description: The CM_Disconnect_Machine function removes a connection to a remote machine.
helpviewer_keywords: ["CM_Disconnect_Machine","CM_Disconnect_Machine function [Device and Driver Installation]","cfgmgr32/CM_Disconnect_Machine","cfgmgrfn_e3549f15-0066-4ace-9b50-45ecf20cce87.xml","devinst.cm_disconnect_machine"]
old-location: devinst\cm_disconnect_machine.htm
tech.root: devinst
ms.assetid: 8318eb7e-f0fa-4b2a-b82d-e8f830665c9d
ms.date: 12/05/2018
ms.keywords: CM_Disconnect_Machine, CM_Disconnect_Machine function [Device and Driver Installation], cfgmgr32/CM_Disconnect_Machine, cfgmgrfn_e3549f15-0066-4ace-9b50-45ecf20cce87.xml, devinst.cm_disconnect_machine
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Disconnect_Machine
 - cfgmgr32/CM_Disconnect_Machine
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
api_name:
 - CM_Disconnect_Machine
---

# CM_Disconnect_Machine function


## -description

<p class="CCE_Message">[Beginning in Windows 8 and Windows Server 2012 functionality to access remote machines has been removed. You cannot access remote machines when running on these versions of Windows.]

The <b>CM_Disconnect_Machine</b> function removes a connection to a remote machine.

## -parameters

### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.