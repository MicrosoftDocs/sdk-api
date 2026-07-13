---
UID: NF:iscsidsc.GetIScsiInitiatorNodeNameW
title: GetIScsiInitiatorNodeNameW function (iscsidsc.h)
description: The GetIscsiInitiatorNodeName function retrieves the common initiator node name that is used when establishing sessions from the local machine. (Unicode)
helpviewer_keywords: ["GetIScsiInitiatorNodeNameW", "GetIscsiInitiatorNodeName", "GetIscsiInitiatorNodeName function [iSCSI Discovery Library API]", "GetIscsiInitiatorNodeNameW", "iscsidisc.getiscsiinitiatornodename", "iscsidsc/GetIscsiInitiatorNodeName", "iscsidsc/GetIscsiInitiatorNodeNameW"]
old-location: iscsidisc\getiscsiinitiatornodename.htm
tech.root: iSCSIDisc
ms.assetid: 592d9cd8-5944-479c-ba21-7cf911e0a5b9
ms.date: 12/05/2018
ms.keywords: GetIScsiInitiatorNodeNameW, GetIscsiInitiatorNodeName, GetIscsiInitiatorNodeName function [iSCSI Discovery Library API], GetIscsiInitiatorNodeNameA, GetIscsiInitiatorNodeNameW, iscsidisc.getiscsiinitiatornodename, iscsidsc/GetIscsiInitiatorNodeName, iscsidsc/GetIscsiInitiatorNodeNameA, iscsidsc/GetIscsiInitiatorNodeNameW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetIscsiInitiatorNodeNameW (Unicode) and GetIscsiInitiatorNodeNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetIScsiInitiatorNodeNameW
 - iscsidsc/GetIScsiInitiatorNodeNameW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-storage-iscsidsc-l1-1-0.dll
 - Iscsidsc.dll
api_name:
 - GetIscsiInitiatorNodeName
 - GetIscsiInitiatorNodeNameA
 - GetIscsiInitiatorNodeNameW
---

# GetIScsiInitiatorNodeNameW function


## -description

The <b>GetIscsiInitiatorNodeName</b> function retrieves the common initiator node name that is used when establishing sessions from the local machine.

## -parameters

### -param InitiatorNodeName

A caller-allocated buffer that, on output, receives the node name. The buffer must be large enough to hold <b>MAX_ISCSI_NAME_LEN+1</b> bytes.

## -returns

Returns ERROR_SUCCESS if the operation succeeds and the appropriate Win32 or iSCSI error code if the operation fails.

## -remarks

All initiator Host Bus Adapters, both software and hardware, use the same node name when establishing sessions.




> [!NOTE]
> The iscsidsc.h header defines GetIScsiInitiatorNodeName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

