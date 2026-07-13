---
UID: NF:lmalert.ALERT_OTHER_INFO
title: ALERT_OTHER_INFO macro (lmalert.h)
description: The ALERT_OTHER_INFO macro returns a pointer to the alert-specific data in an alert message. The data follows a STD_ALERT structure, and can be an ADMIN_OTHER_INFO, a PRINT_OTHER_INFO, or a USER_OTHER_INFO structure.
helpviewer_keywords: ["ALERT_OTHER_INFO","ALERT_OTHER_INFO macro [Network Management]","_win32_alert_other_info","lmalert/ALERT_OTHER_INFO","netmgmt.alert_other_info"]
old-location: netmgmt\alert_other_info.htm
tech.root: NetMgmt
ms.assetid: e7bcc306-4b44-4230-96aa-a4717bb1fb11
ms.date: 07/01/2025
ms.keywords: ALERT_OTHER_INFO, ALERT_OTHER_INFO macro [Network Management], _win32_alert_other_info, lmalert/ALERT_OTHER_INFO, netmgmt.alert_other_info
req.header: lmalert.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ALERT_OTHER_INFO
 - lmalert/ALERT_OTHER_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmalert.h
api_name:
 - ALERT_OTHER_INFO
---

# ALERT_OTHER_INFO macro

## -syntax

```cpp
LPBYTE ALERT_OTHER_INFO(
    LPBYTE x
);
```

## -returns

Type: **LPBYTE**

The return value is a pointer to the fixed-length structure that follows the <a href="/windows/desktop/api/lmalert/ns-lmalert-std_alert">STD_ALERT</a> structure in the alert message.


## -description

The <b>ALERT_OTHER_INFO</b> macro returns a pointer to the alert-specific data in an alert message. The data follows a <a href="/windows/desktop/api/lmalert/ns-lmalert-std_alert">STD_ALERT</a> structure, and can be an <a href="/windows/desktop/api/lmalert/ns-lmalert-admin_other_info">ADMIN_OTHER_INFO</a>, a <a href="/windows/desktop/api/lmalert/ns-lmalert-print_other_info">PRINT_OTHER_INFO</a>, or a <a href="/windows/desktop/api/lmalert/ns-lmalert-user_other_info">USER_OTHER_INFO</a> structure.

## -parameters

### -param x

Pointer to a <b>STD_ALERT</b> structure that was specified in a call to the <a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a> function.

## -remarks

The 
<b>ALERT_OTHER_INFO</b> macro is defined as follows:


```cpp
#include <windows.h>

#define ALERT_OTHER_INFO(x)    ((LPBYTE)(x) + sizeof(STD_ALERT))


```


See <a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a> for a code sample that uses the <b>ALERT_OTHER_INFO</b> macro to retrieve a pointer to the <b>ADMIN_OTHER_INFO</b> structure.

## -see-also

<a href="/windows/desktop/api/lmalert/ns-lmalert-admin_other_info">ADMIN_OTHER_INFO</a>

<a href="/windows/desktop/api/lmalert/nf-lmalert-alert_var_data">ALERT_VAR_DATA</a>

<a href="/windows/desktop/NetMgmt/alert-functions">Alert Functions</a>

<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a>

<a href="/windows/desktop/NetMgmt/network-management-macros">Network
		  Management Macros</a>

<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>

<a href="/windows/desktop/api/lmalert/ns-lmalert-print_other_info">PRINT_OTHER_INFO</a>

<a href="/windows/desktop/api/lmalert/ns-lmalert-std_alert">STD_ALERT</a>

<a href="/windows/desktop/api/lmalert/ns-lmalert-user_other_info">USER_OTHER_INFO</a>
