---
UID: NF:lmalert.ALERT_VAR_DATA
title: ALERT_VAR_DATA macro (lmalert.h)
description: The ALERT_VAR_DATA macro returns a pointer to the variable-length portion of an alert message. Variable-length data can follow an ADMIN_OTHER_INFO, a PRINT_OTHER_INFO, or a USER_OTHER_INFO structure.helpviewer_keywords: ["ALERT_VAR_DATA","ALERT_VAR_DATA macro [Network Management]","_win32_alert_var_data","lmalert/ALERT_VAR_DATA","netmgmt.alert_var_data"]
old-location: netmgmt\alert_var_data.htm
tech.root: NetMgmt
ms.assetid: ff71fb3d-8c01-47ac-93f2-108b1f49e2da
ms.date: 12/05/2018
ms.keywords: ALERT_VAR_DATA, ALERT_VAR_DATA macro [Network Management], _win32_alert_var_data, lmalert/ALERT_VAR_DATA, netmgmt.alert_var_data
f1_keywords:
- lmalert/ALERT_VAR_DATA
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Lmalert.h
api_name:
- ALERT_VAR_DATA
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ALERT_VAR_DATA macro


## -description


The 
				<b>ALERT_VAR_DATA</b> macro returns a pointer to the variable-length portion of an alert message. Variable-length data can follow an 
<a href="https://docs.microsoft.com/windows/desktop/api/lmalert/ns-lmalert-admin_other_info">ADMIN_OTHER_INFO</a>, a 
<a href="https://docs.microsoft.com/windows/desktop/api/lmalert/ns-lmalert-print_other_info">PRINT_OTHER_INFO</a>, or a 
<a href="https://docs.microsoft.com/windows/desktop/api/lmalert/ns-lmalert-user_other_info">USER_OTHER_INFO</a> structure.


## -parameters




### -param p

Pointer to an 
<b>ADMIN_OTHER_INFO</b>, a 
<b>PRINT_OTHER_INFO</b>, or a 
<b>USER_OTHER_INFO</b> structure that was specified in a call to the 
<a href="https://docs.microsoft.com/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a> function or the 
<a href="https://docs.microsoft.com/windows/desktop/api/lmalert/nf-lmalert-netalertraiseex">NetAlertRaiseEx</a> function.


## -remarks



The 
<b>ALERT_VAR_DATA</b> macro is defined as follows:


```cpp
#include <windows.h>

#define ALERT_VAR_DATA(p)      ((LPBYTE)(p) + sizeof(*p))


```


See 
<a href="https://docs.microsoft.com/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/lmalert/nf-lmalert-netalertraiseex">NetAlertRaiseEx</a> for code samples that use the 
<b>ALERT_VAR_DATA</b> macro to retrieve a pointer to the variable-length data in an alert message.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lmalert/ns-lmalert-admin_other_info">ADMIN_OTHER_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmalert/nf-lmalert-alert_other_info">ALERT_OTHER_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/alert-functions">Alert Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmalert/nf-lmalert-netalertraiseex">NetAlertRaiseEx</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-macros">Network
		  Management Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmalert/ns-lmalert-print_other_info">PRINT_OTHER_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmalert/ns-lmalert-user_other_info">USER_OTHER_INFO</a>
 

 

