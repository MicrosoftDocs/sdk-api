---
UID: NF:winbase.OperationEnd
title: OperationEnd function (winbase.h)
description: Notifies the system that the application is about to end an operation.
helpviewer_keywords: ["OperationEnd","OperationEnd function [Operation Recorder]","oprec.operationend","winbase/OperationEnd"]
old-location: oprec\operationend.htm
tech.root: oprec
ms.assetid: 73C6FBDD-BB4A-46A5-8E39-7862A1938F47
ms.date: 12/05/2018
ms.keywords: OperationEnd, OperationEnd function [Operation Recorder], oprec.operationend, winbase/OperationEnd
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OperationEnd
 - winbase/OperationEnd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - OperationEnd
---

# OperationEnd function


## -description

Notifies the system that the application is about to end an operation

Every call to <a href="/windows/desktop/api/winbase/nf-winbase-operationstart">OperationStart</a> must be followed by a call to <b>OperationEnd</b>, otherwise the operation's record of file access patterns is discarded after 10 seconds.

## -parameters

### -param OperationEndParams [in]

An <a href="/windows/desktop/api/winbase/ns-winbase-operation_end_parameters">_OPERATION_END_PARAMETERS</a> structure that specifies <b>VERSION</b>, <b>OPERATION_ID</b> and <b>FLAGS</b>.

## -returns

<b>TRUE</b> for all valid parameters and <b>FALSE</b> otherwise.  To get extended error information, call <b>GetLastError</b>.

## -remarks

The version of the <a href="/windows/desktop/api/winbase/ns-winbase-operation_end_parameters">_OPERATION_END_PARAMETERS</a> structure is defined as <b>OPERATION_API_VERSION</b> in the Windows SDK. 

The  <b>OperationEnd</b> function is safe to call on any thread.

## -see-also

<b></b>



<a href="/previous-versions/windows/desktop/oprec/operation-id">OPERATION_ID</a>



<a href="/previous-versions/windows/desktop/oprec/-operation-portal">Operation Recorder</a>



<a href="/windows/desktop/api/winbase/nf-winbase-operationstart">OperationStart</a>



<a href="/windows/desktop/api/winbase/ns-winbase-operation_end_parameters">_OPERATION_END_PARAMETERS</a>



<a href="/windows/desktop/api/winbase/ns-winbase-operation_start_parameters">_OPERATION_START_PARAMETERS</a>