---
UID: NF:avrt.AvRtLeaveThreadOrderingGroup
title: AvRtLeaveThreadOrderingGroup function (avrt.h)
description: Enables client threads to leave a thread ordering group.
helpviewer_keywords: ["AvRtLeaveThreadOrderingGroup","AvRtLeaveThreadOrderingGroup function","avrt/AvRtLeaveThreadOrderingGroup","base.avrtleavethreadorderinggroup"]
old-location: base\avrtleavethreadorderinggroup.htm
tech.root: backup
ms.assetid: b618c312-0a43-4815-ad32-8820c658dc0b
ms.date: 12/05/2018
ms.keywords: AvRtLeaveThreadOrderingGroup, AvRtLeaveThreadOrderingGroup function, avrt/AvRtLeaveThreadOrderingGroup, base.avrtleavethreadorderinggroup
req.header: avrt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Avrt.lib
req.dll: Avrt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AvRtLeaveThreadOrderingGroup
 - avrt/AvRtLeaveThreadOrderingGroup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avrt.dll
api_name:
 - AvRtLeaveThreadOrderingGroup
---

# AvRtLeaveThreadOrderingGroup function


## -description

Enables client threads to leave a thread ordering group.

## -parameters

### -param Context [in]

A context handle. This handle is returned by the <a href="/windows/desktop/api/avrt/nf-avrt-avrtjointhreadorderinggroup">AvRtJoinThreadOrderingGroup</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The parent thread for a thread ordering group should not remove itself from the group.

If a thread times out and attempts to call this function, the function fails with a last error code of ERROR_INVALID_PARAMETER.

## -see-also

<a href="/windows/desktop/ProcThread/thread-ordering-service">Thread Ordering Service</a>