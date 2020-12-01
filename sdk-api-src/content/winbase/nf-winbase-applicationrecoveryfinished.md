---
UID: NF:winbase.ApplicationRecoveryFinished
title: ApplicationRecoveryFinished function (winbase.h)
description: Indicates that the calling application has completed its data recovery.
helpviewer_keywords: ["ApplicationRecoveryFinished","ApplicationRecoveryFinished function [Recovery]","recovery.applicationrecoveryfinished","winbase/ApplicationRecoveryFinished"]
old-location: recovery\applicationrecoveryfinished.htm
tech.root: Recovery
ms.assetid: 2c9309c5-c36d-4b68-a642-ed087024dba1
ms.date: 12/05/2018
ms.keywords: ApplicationRecoveryFinished, ApplicationRecoveryFinished function [Recovery], recovery.applicationrecoveryfinished, winbase/ApplicationRecoveryFinished
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ApplicationRecoveryFinished
 - winbase/ApplicationRecoveryFinished
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - ApplicationRecoveryFinished
---

# ApplicationRecoveryFinished function


## -description

Indicates that  the calling application has completed its data recovery.

## -parameters

### -param bSuccess [in]

Specify <b>TRUE</b> to indicate that the data was successfully recovered; otherwise, <b>FALSE</b>.

## -remarks

This should be the last call that you make in your callback because your application terminates as soon as this function is called.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-applicationrecoveryinprogress">ApplicationRecoveryInProgress</a>



<a href="/windows/desktop/api/winbase/nf-winbase-registerapplicationrecoverycallback">RegisterApplicationRecoveryCallback</a>