---
UID: NF:cfgmgr32.CM_Disconnect_Machine
title: CM_Disconnect_Machine function
author: windows-sdk-content
description: The CM_Disconnect_Machine function removes a connection to a remote machine.
old-location: devinst\cm_disconnect_machine.htm
old-project: devinst
ms.assetid: 8318eb7e-f0fa-4b2a-b82d-e8f830665c9d
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CM_Disconnect_Machine, CM_Disconnect_Machine function [Device and Driver Installation], cfgmgr32/CM_Disconnect_Machine, cfgmgrfn_e3549f15-0066-4ace-9b50-45ecf20cce87.xml, devinst.cm_disconnect_machine
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.redist: 
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
tech.root: 
req.typenames: CM_NOTIFY_ACTION, *PCM_NOTIFY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
api_name:
 - CM_Disconnect_Machine
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
---

# CM_Disconnect_Machine function


## -description


<p class="CCE_Message">[Beginning in Windows 8 and Windows Server 2012 functionality to access remote machines has been removed. You cannot access remote machines when running on these versions of Windows.]

The <b>CM_Disconnect_Machine</b> function removes a connection to a remote machine.




## -parameters




### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="https://msdn.microsoft.com/4108a35f-0861-4142-a798-731287515910">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.



