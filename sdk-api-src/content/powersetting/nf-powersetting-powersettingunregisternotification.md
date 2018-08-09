---
UID: NF:powersetting.PowerSettingUnregisterNotification
title: PowerSettingUnregisterNotification function
author: windows-sdk-content
description: Cancels a registration to receive notification when a power setting changes.
old-location: base\powersettingunregisternotification.htm
old-project: power
ms.assetid: 9853c347-4528-43bb-8326-13bcd819b8a6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PowerSettingUnregisterNotification, PowerSettingUnregisterNotification function, base.powersettingunregisternotification, powersetting/PowerSettingUnregisterNotification, powrprof/PowerSettingUnregisterNotification
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: powersetting.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Powrprof.dll
 - API-MS-Win-power-setting-l1-1-0.dll
api_name:
 - PowerSettingUnregisterNotification
product: Windows
targetos: Windows
req.lib: Powrprof.lib
req.dll: Powrprof.dll
req.irql: 
req.product: ADAM
---

# PowerSettingUnregisterNotification function


## -description


Cancels a registration to receive notification when a power setting changes.


## -parameters




### -param RegistrationHandle [in, out]

A handle to a registration obtained by calling the <a href="https://msdn.microsoft.com/0fbca717-2367-4407-8094-3eb2b717b59c">PowerSettingRegisterNotification</a> function.


## -returns



Returns ERROR_SUCCESS (zero) if the call was successful, and a nonzero value if the call failed.




## -see-also




<a href="https://msdn.microsoft.com/0fbca717-2367-4407-8094-3eb2b717b59c">PowerSettingRegisterNotification</a>
 

 

