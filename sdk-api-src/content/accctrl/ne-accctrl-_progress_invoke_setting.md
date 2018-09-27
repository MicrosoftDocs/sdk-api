---
UID: NE:accctrl._PROGRESS_INVOKE_SETTING
title: "_PROGRESS_INVOKE_SETTING"
author: windows-sdk-content
description: Indicates the initial setting of the function used to track the progress of a call to the TreeSetNamedSecurityInfo or TreeResetNamedSecurityInfo function.
old-location: security\prog_invoke_setting.htm
tech.root: secauthz
ms.assetid: 3eee30d6-7d9d-468f-b6ba-e172da523169
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PPROG_INVOKE_SETTING, PPROG_INVOKE_SETTING, PPROG_INVOKE_SETTING enumeration pointer [Security], PROG_INVOKE_SETTING, PROG_INVOKE_SETTING enumeration [Security], ProgressCancelOperation, ProgressInvokeEveryObject, ProgressInvokeNever, ProgressInvokeOnError, ProgressInvokePrePostError, ProgressRetryOperation, _PROGRESS_INVOKE_SETTING, accctrl/PPROG_INVOKE_SETTING, accctrl/PROG_INVOKE_SETTING, accctrl/ProgressCancelOperation, accctrl/ProgressInvokeEveryObject, accctrl/ProgressInvokeNever, accctrl/ProgressInvokeOnError, accctrl/ProgressInvokePrePostError, accctrl/ProgressRetryOperation, security.prog_invoke_setting"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AccCtrl.h
api_name:
 - PROG_INVOKE_SETTING
product: Windows
targetos: Windows
req.typenames: PROG_INVOKE_SETTING, *PPROG_INVOKE_SETTING
req.redist: 
---

# _PROGRESS_INVOKE_SETTING enumeration


## -description


The <b>PROG_INVOKE_SETTING</b> enumeration indicates the initial setting of the function used to track the progress of a call to the <a href="https://msdn.microsoft.com/caa711c3-301b-4ed7-b1f4-dc6a48563905">TreeSetNamedSecurityInfo</a> or <a href="https://msdn.microsoft.com/adae7d07-a452-409e-b1a1-e9f86f873e39">TreeResetNamedSecurityInfo</a> function.


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

