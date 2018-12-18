---
UID: NF:cfgmgr32.CM_Open_Class_KeyW
title: CM_Open_Class_KeyW function
author: windows-sdk-content
description: The CM_Open_Class_Key function opens the device setup class registry key, the device interface class registry key, or a specific subkey of a class.
old-location: devinst\cm_open_class_key.htm
tech.root: devinst
ms.assetid: 5a87769e-3555-44ce-b4d8-16c98bdc3732
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CM_Open_Class_Key, CM_Open_Class_Key function [Device and Driver Installation], CM_Open_Class_KeyW, cfgmgr32/CM_Open_Class_Key, cfgmgr32/CM_Open_Class_KeyW, cfgmgrfn_70b86a61-c687-4d43-8c3f-8a00db441580.xml, devinst.cm_open_class_key
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
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/f315f5fa-eb67-4898-ac4e-acb92b8e9b3e">CM_Delete_Class_Key</a>



<a href="https://msdn.microsoft.com/c931f906-8237-4203-b9b6-4dd54a93ca8b">SetupDiOpenClassRegKeyEx</a>
 

 

