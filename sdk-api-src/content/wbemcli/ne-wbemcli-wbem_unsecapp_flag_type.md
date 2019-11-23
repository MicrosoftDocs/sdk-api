---
UID: NE:wbemcli.tag_WBEM_UNSECAPP_FLAG_TYPE
title: WBEM_UNSECAPP_FLAG_TYPE (wbemcli.h)

description: Used to control access checks on callbacks when using the IWbemUnsecuredApartment::CreateSinkStub method.
old-location: wmi\wbem_unsecapp_flag_type.htm
tech.root: WmiSdk
ms.assetid: DE009790-86D0-4030-AC28-F04DD6601261

ms.date: 12/05/2018
ms.keywords: WBEM_FLAG_UNSECAPP_CHECK_ACCESS, WBEM_FLAG_UNSECAPP_DEFAULT_CHECK_ACCESS, WBEM_FLAG_UNSECAPP_DONT_CHECK_ACCESS, WBEM_UNSECAPP_FLAG_TYPE, WBEM_UNSECAPP_FLAG_TYPE enumeration [Windows Management Instrumentation], wbemcli/WBEM_FLAG_UNSECAPP_CHECK_ACCESS, wbemcli/WBEM_FLAG_UNSECAPP_DEFAULT_CHECK_ACCESS, wbemcli/WBEM_FLAG_UNSECAPP_DONT_CHECK_ACCESS, wbemcli/WBEM_UNSECAPP_FLAG_TYPE, wmi.wbem_unsecapp_flag_type
ms.topic: enum
f1_keywords: 
 - "wbemcli/WBEM_UNSECAPP_FLAG_TYPE"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemcli.h
api_name:
 - WBEM_UNSECAPP_FLAG_TYPE
targetos: Windows
req.typenames: WBEM_UNSECAPP_FLAG_TYPE
req.redist: 
ms.custom: 19H1
---

# WBEM_UNSECAPP_FLAG_TYPE enumeration


## -description


Used to control access checks on callbacks when using the <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub">IWbemUnsecuredApartment::CreateSinkStub</a> method.


## -enum-fields




### -field WBEM_FLAG_UNSECAPP_DEFAULT_CHECK_ACCESS

Unsecapp.exe reads the registry key UnsecAppAccessControlDefault to determine if it should authenticate callbacks.


### -field WBEM_FLAG_UNSECAPP_CHECK_ACCESS

Unsecapp.exe authenticates callbacks regardless of the setting of the registry key UnsecAppAccessControlDefault.


### -field WBEM_FLAG_UNSECAPP_DONT_CHECK_ACCESS

Unsecapp.exe does not authenticate callbacks regardless of the setting of the registry key UnsecAppAccessControlDefault.

