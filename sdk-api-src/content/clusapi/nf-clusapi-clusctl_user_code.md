---
UID: NF:clusapi.CLUSCTL_USER_CODE
title: CLUSCTL_USER_CODE macro (clusapi.h)
description: Generates a correctly formatted user-defined control code. For more information on the bit layout of control codes, see Control Code Architecture.
helpviewer_keywords: ["0","1","2","CLUSCTL_USER_CODE","CLUSCTL_USER_CODE macro [Failover Cluster]","_wolf_clusctl_user_code","clusapi/CLUSCTL_USER_CODE","mscs.clusctl_user_code"]
old-location: mscs\clusctl_user_code.htm
tech.root: MsCS
ms.assetid: b21a565a-df43-486c-a474-2dc6d2f45197
ms.date: 12/05/2018
ms.keywords: 0, 1, 2, CLUSCTL_USER_CODE, CLUSCTL_USER_CODE macro [Failover Cluster], _wolf_clusctl_user_code, clusapi/CLUSCTL_USER_CODE, mscs.clusctl_user_code
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - CLUSCTL_USER_CODE
 - clusapi/CLUSCTL_USER_CODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSCTL_USER_CODE
---

# CLUSCTL_USER_CODE macro


## -description

Generates a correctly 
    formatted user-defined control code. For more information on the bit layout of control codes, see 
    <a href="/previous-versions/windows/desktop/mscs/control-code-architecture">Control Code Architecture</a>.

## -parameters

### -param Function

Value that specifies the operation code (bits 0–23) and, optionally, the access code 
     (bits 0–1) of the resulting control code. The operation code can be any 19-bit value chosen 
     by the caller. The access code (if specified) should be set to one of the following values.



#### 0 (CLUS_ACCESS_ANY)

The control code has no access requirements.



#### 1 (CLUS_ACCESS_READ)

Use of the control code requires read access.



#### 2 (CLUS_ACCESS_WRITE)

Use of the control code requires write access.

### -param Object

An 8-bit value that specifies the object code (bits 24–31) of the resulting control 
      code. For more information on the bit layout of control codes, see 
      <a href="/previous-versions/windows/desktop/mscs/control-code-architecture">Control Code Architecture</a>. The 
      object code can be set to any value greater than <b>CLUS_OBJECT_USER</b> (128).

## -remarks

Do not pass bit-shifted values for <i>Function</i> or <i>Object</i>. The 
    macro performs the required bit shifts.

If no access code is specified, the control code will default to 
    <b>CLUS_ACCESS_ANY</b>.


#### Examples

See the example under 
     <a href="/previous-versions/windows/desktop/mscs/creating-control-codes">Creating Control Codes</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusctl_get_access_mode">CLUSCTL_GET_ACCESS_MODE</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusctl_get_control_function">CLUSCTL_GET_CONTROL_FUNCTION</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusctl_get_control_object">CLUSCTL_GET_CONTROL_OBJECT</a>