---
UID: NE:accctrl._PROGRESS_INVOKE_SETTING
title: PROG_INVOKE_SETTING (accctrl.h)
description: Indicates the initial setting of the function used to track the progress of a call to the TreeSetNamedSecurityInfo or TreeResetNamedSecurityInfo function.
helpviewer_keywords: ["*PPROG_INVOKE_SETTING","PPROG_INVOKE_SETTING","PPROG_INVOKE_SETTING enumeration pointer [Security]","PROG_INVOKE_SETTING","PROG_INVOKE_SETTING enumeration [Security]","ProgressCancelOperation","ProgressInvokeEveryObject","ProgressInvokeNever","ProgressInvokeOnError","ProgressInvokePrePostError","ProgressRetryOperation","accctrl/PPROG_INVOKE_SETTING","accctrl/PROG_INVOKE_SETTING","accctrl/ProgressCancelOperation","accctrl/ProgressInvokeEveryObject","accctrl/ProgressInvokeNever","accctrl/ProgressInvokeOnError","accctrl/ProgressInvokePrePostError","accctrl/ProgressRetryOperation","security.prog_invoke_setting"]
old-location: security\prog_invoke_setting.htm
tech.root: security
ms.assetid: 3eee30d6-7d9d-468f-b6ba-e172da523169
ms.date: 12/05/2018
ms.keywords: '*PPROG_INVOKE_SETTING, PPROG_INVOKE_SETTING, PPROG_INVOKE_SETTING enumeration pointer [Security], PROG_INVOKE_SETTING, PROG_INVOKE_SETTING enumeration [Security], ProgressCancelOperation, ProgressInvokeEveryObject, ProgressInvokeNever, ProgressInvokeOnError, ProgressInvokePrePostError, ProgressRetryOperation, accctrl/PPROG_INVOKE_SETTING, accctrl/PROG_INVOKE_SETTING, accctrl/ProgressCancelOperation, accctrl/ProgressInvokeEveryObject, accctrl/ProgressInvokeNever, accctrl/ProgressInvokeOnError, accctrl/ProgressInvokePrePostError, accctrl/ProgressRetryOperation, security.prog_invoke_setting'
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: PROG_INVOKE_SETTING, *PPROG_INVOKE_SETTING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROGRESS_INVOKE_SETTING
 - accctrl/_PROGRESS_INVOKE_SETTING
 - PPROG_INVOKE_SETTING
 - accctrl/PPROG_INVOKE_SETTING
 - PROG_INVOKE_SETTING
 - accctrl/PROG_INVOKE_SETTING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AccCtrl.h
api_name:
 - PROG_INVOKE_SETTING
---

# PROG_INVOKE_SETTING enumeration


## -description

The <b>PROG_INVOKE_SETTING</b> enumeration indicates the initial setting of the function used to track the progress of a call to the <a href="/windows/desktop/api/aclapi/nf-aclapi-treesetnamedsecurityinfoa">TreeSetNamedSecurityInfo</a> or <a href="/windows/desktop/api/aclapi/nf-aclapi-treeresetnamedsecurityinfoa">TreeResetNamedSecurityInfo</a> function.

## -enum-fields

### -field ProgressInvokeNever

Never invoke the progress function.

### -field ProgressInvokeEveryObject

Invoke the progress function for every object.

### -field ProgressInvokeOnError

Invoke the progress function only when an error is encountered.

### -field ProgressCancelOperation

Discontinue the tree operation.

<div class="alert"><b>Note</b>  The original state of the tree will not be reset, and the results are unpredictable.</div>
<div> </div>

### -field ProgressRetryOperation

Retry the tree operation.

### -field ProgressInvokePrePostError

Invoke the progress function before and after applying security on the object and on the error.