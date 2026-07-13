---
UID: NF:cfgmgr32.CM_Uninstall_DevNode
title: CM_Uninstall_DevNode function (cfgmgr32.h)
description: The CM_Uninstall_DevNode function removes all persistent state associated with a device instance.
helpviewer_keywords: ["CM_Uninstall_DevNode","CM_Uninstall_DevNode function [Device and Driver Installation]","cfgmgr32/CM_Uninstall_DevNode","cfgmgrfn_a3aadd47-2a1b-4123-823f-7d7cb988812e.xml","devinst.cm_uninstall_devnode"]
old-location: devinst\cm_uninstall_devnode.htm
tech.root: devinst
ms.assetid: e472e642-cf0d-4c88-907f-5cfb08fb4e76
ms.date: 12/05/2018
ms.keywords: CM_Uninstall_DevNode, CM_Uninstall_DevNode function [Device and Driver Installation], cfgmgr32/CM_Uninstall_DevNode, cfgmgrfn_a3aadd47-2a1b-4123-823f-7d7cb988812e.xml, devinst.cm_uninstall_devnode
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
req.lib: Cfgmgr32.lib; OneCoreUAP.lib on Windows 10
req.dll: CfgMgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Uninstall_DevNode
 - cfgmgr32/CM_Uninstall_DevNode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-devices-config-l1-1-2.dll
 - CfgMgr32.dll
 - API-MS-Win-devices-config-l1-1-0.dll
 - API-MS-Win-devices-config-l1-1-1.dll
api_name:
 - CM_Uninstall_DevNode
---

# CM_Uninstall_DevNode function


## -description

The <b>CM_Uninstall_DevNode</b> function removes all persistent state associated with a device instance.

## -parameters

### -param dnDevInst [in]

Device instance handle that is bound to the local machine.

### -param ulFlags [in]

Reserved. Must be set to zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

This function uninstalls the device without sending an <b>IRP_MN_QUERY_REMOVE_DEVICE</b> request or calling class installers or co-installers.       If your application will run only on a <a href="/windows-hardware/drivers/develop/windows-10-editions-for-universal-drivers">Target Platform</a> of Desktop, instead of calling <b>CM_Uninstall_DevNode</b>, the application should uninstall the device by calling <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a> with the <a href="/windows-hardware/drivers/install/dif-remove">DIF_REMOVE</a> code, or by calling <a href="/windows/desktop/api/newdev/nf-newdev-diuninstalldevice">DiUninstallDevice</a>.

Use the following sequence to call this function:

<ol>
<li>Check if <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_devnode_status">CM_Get_DevNode_Status</a> returns success.  This means that the device is present.</li>
<li>If the device is present, call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew">CM_Query_And_Remove_SubTree</a>.</li>
<li>Call <b>CM_Uninstall_DevNode</b>.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a>