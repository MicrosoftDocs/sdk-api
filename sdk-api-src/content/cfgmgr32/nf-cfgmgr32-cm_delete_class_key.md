---
UID: NF:cfgmgr32.CM_Delete_Class_Key
title: CM_Delete_Class_Key function (cfgmgr32.h)
description: The CM_Delete_Class_Key function removes the specified installed device class from the system.
helpviewer_keywords: ["CM_Delete_Class_Key","CM_Delete_Class_Key function [Device and Driver Installation]","cfgmgr32/CM_Delete_Class_Key","cfgmgrfn_4e8a0362-3fd5-4cb6-af2b-33a904bcafde.xml","devinst.cm_delete_class_key"]
old-location: devinst\cm_delete_class_key.htm
tech.root: devinst
ms.assetid: f315f5fa-eb67-4898-ac4e-acb92b8e9b3e
ms.date: 12/05/2018
ms.keywords: CM_Delete_Class_Key, CM_Delete_Class_Key function [Device and Driver Installation], cfgmgr32/CM_Delete_Class_Key, cfgmgrfn_4e8a0362-3fd5-4cb6-af2b-33a904bcafde.xml, devinst.cm_delete_class_key
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
 - CM_Delete_Class_Key
 - cfgmgr32/CM_Delete_Class_Key
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
 - CM_Delete_Class_Key
---

# CM_Delete_Class_Key function


## -description

The <b>CM_Delete_Class_Key</b> function removes the specified installed <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device class</a> from the system.

## -parameters

### -param ClassGuid [in]

Pointer to the GUID of the device class to remove.

### -param ulFlags [in]

Delete class key flags:





#### CM_DELETE_CLASS_ONLY

Delete the class only if it does not contain any subkeys.



#### CM_DELETE_CLASS_SUBKEYS

Delete the class and all of its subkeys.



#### CM_DELETE_CLASS_INTERFACE (available only in Windows Vista and later)

Indicates that <i>ClassGuid</i> specifies a <a href="/windows-hardware/drivers/install/overview-of-device-interface-classes">device interface class</a> and not a <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a>.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_class_keyw">CM_Open_Class_Key</a>