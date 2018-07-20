---
UID: NF:cfgmgr32.CM_Open_Class_KeyW
title: CM_Open_Class_KeyW function
author: windows-sdk-content
description: The CM_Open_Class_Key function opens the device setup class registry key, the device interface class registry key, or a specific subkey of a class.
old-location: devinst\cm_open_class_key.htm
old-project: devinst
ms.assetid: 5a87769e-3555-44ce-b4d8-16c98bdc3732
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: CM_Open_Class_Key, CM_Open_Class_Key function [Device and Driver Installation], CM_Open_Class_KeyW, cfgmgr32/CM_Open_Class_Key, cfgmgr32/CM_Open_Class_KeyW, cfgmgrfn_70b86a61-c687-4d43-8c3f-8a00db441580.xml, devinst.cm_open_class_key
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Open_Class_KeyW (Unicode)
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
 - Cfgmgr32.lib
 - Cfgmgr32.dll
 - API-Ms-Win-Devices-Config-L1-1-0.dll
 - API-Ms-Win-Devices-Config-L1-1-1.dll
 - CfgMgr32.dll
api_name:
 - CM_Open_Class_Key
 - CM_Open_Class_KeyW
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
---

# CM_Open_Class_KeyW function


## -description


The <b>CM_Open_Class_Key</b> function opens the device setup class registry key, the device interface class registry key, or a specific subkey of a class.


## -parameters




### -param ClassGuid [in, optional]

Pointer to the GUID of the class whose registry key is to be opened. This parameter is optional and can be NULL. If this parameter is NULL, the root of the class tree is opened.


### -param pszClassName [in, optional]

Reserved. Must be set to NULL.


### -param samDesired [in]

The registry security access for the key to be opened.


### -param Disposition [in]

Specifies how the registry key is to be opened. May be one of the following values:





#### RegDisposition_OpenAlways

Open the key if it exists. Otherwise, create the key.



#### RegDisposition_OpenExisting

Open the key only if it exists.


### -param phkClass [out]

Pointer to an HKEY that will receive the opened key upon success.


### -param ulFlags [in]

Open class key flags:





#### CM_OPEN_CLASS_KEY_INSTALLER

The key to be opened is for a device setup class.



#### CM_OPEN_CLASS_KEY_INTERFACE

The key to be opened is for a device interface class.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



Close the handle returned from this function by calling <b>RegCloseKey</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537966">CM_Delete_Class_Key</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552067">SetupDiOpenClassRegKeyEx</a>
 

 

