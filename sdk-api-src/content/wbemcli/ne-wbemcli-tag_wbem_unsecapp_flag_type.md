---
UID: NE:wbemcli.tag_WBEM_UNSECAPP_FLAG_TYPE
title: tag_WBEM_UNSECAPP_FLAG_TYPE
author: windows-sdk-content
description: Used to control access checks on callbacks when using the IWbemUnsecuredApartment::CreateSinkStub method.
old-location: wmi\wbem_unsecapp_flag_type.htm
old-project: WmiSdk
ms.assetid: DE009790-86D0-4030-AC28-F04DD6601261
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: WBEM_FLAG_UNSECAPP_CHECK_ACCESS, WBEM_FLAG_UNSECAPP_DEFAULT_CHECK_ACCESS, WBEM_FLAG_UNSECAPP_DONT_CHECK_ACCESS, WBEM_UNSECAPP_FLAG_TYPE, WBEM_UNSECAPP_FLAG_TYPE enumeration [Windows Management Instrumentation], tag_WBEM_UNSECAPP_FLAG_TYPE, wbemcli/WBEM_FLAG_UNSECAPP_CHECK_ACCESS, wbemcli/WBEM_FLAG_UNSECAPP_DEFAULT_CHECK_ACCESS, wbemcli/WBEM_FLAG_UNSECAPP_DONT_CHECK_ACCESS, wbemcli/WBEM_UNSECAPP_FLAG_TYPE, wmi.wbem_unsecapp_flag_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wbemcli.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: WBEM_UNSECAPP_FLAG_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemcli.h
api_name:
 - WBEM_UNSECAPP_FLAG_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tag_WBEM_UNSECAPP_FLAG_TYPE enumeration


## -description


Used to control access checks on callbacks when using the <a href="https://msdn.microsoft.com/546ae2f8-c208-4846-a3ba-e124aefe619d">IWbemUnsecuredApartment::CreateSinkStub</a> method.


## -enum-fields




### -field WBEM_FLAG_UNSECAPP_DEFAULT_CHECK_ACCESS

Unsecapp.exe reads the registry key UnsecAppAccessControlDefault to determine if it should authenticate callbacks.


### -field WBEM_FLAG_UNSECAPP_CHECK_ACCESS

Unsecapp.exe authenticates callbacks regardless of the setting of the registry key UnsecAppAccessControlDefault.


### -field WBEM_FLAG_UNSECAPP_DONT_CHECK_ACCESS

Unsecapp.exe does not authenticate callbacks regardless of the setting of the registry key UnsecAppAccessControlDefault.

