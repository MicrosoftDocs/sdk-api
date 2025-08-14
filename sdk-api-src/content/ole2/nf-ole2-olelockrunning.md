---
UID: NF:ole2.OleLockRunning
title: OleLockRunning function (ole2.h)
description: Locks an already running object into its running state or unlocks it from its running state. (OleLockRunning)
helpviewer_keywords: ["OleLockRunning","OleLockRunning function [COM]","_ole_OleLockRunning","com.olelockrunning","ole2/OleLockRunning"]
old-location: com\olelockrunning.htm
tech.root: com
ms.assetid: 84941a59-6880-4824-b4b9-cd1b52d2bffb
ms.date: 12/05/2018
ms.keywords: OleLockRunning, OleLockRunning function [COM], _ole_OleLockRunning, com.olelockrunning, ole2/OleLockRunning
req.header: ole2.h
req.include-header: 
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleLockRunning
 - ole2/OleLockRunning
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - ext-ms-win-com-ole32-l1-1-4.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - ext-ms-win-com-ole32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-1.dll
 - Ole32.dll
 - ext-ms-win-com-ole32-l1-1-0.dll
api_name:
 - OleLockRunning
---

# OleLockRunning function


## -description

Locks an already running object into its running state or unlocks it from its running state.

## -parameters

### -param pUnknown [in]

Pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the object, which the function uses to query for a pointer to <a href="/windows/desktop/api/objidl/nn-objidl-irunnableobject">IRunnableObject</a>.

### -param fLock [in]

<b>TRUE</b> locks the object into its running state. <b>FALSE</b> unlocks the object from its running state.

### -param fLastUnlockCloses [in]

<b>TRUE</b> specifies that if the connection being released is the last external lock on the object, the object should close. <b>FALSE</b> specifies that the object should remain open until closed by the user or another process.

## -returns

This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
</table>

## -remarks

The <b>OleLockRunning</b> function saves you the trouble of calling the <a href="/windows/desktop/api/objidl/nf-objidl-irunnableobject-lockrunning">IRunnableObject::LockRunning</a> method. You can use <b>OleLockRunning</b> and <b>IRunnableObject::LockRunning</b> interchangeably. With the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer passed in with the <i>pUnknown</i> parameter, <b>OleLockRunning</b> queries for an <a href="/windows/desktop/api/objidl/nn-objidl-irunnableobject">IRunnableObject</a> pointer. If successful, it calls <b>IRunnableObject::LockRunning</b> and returns the results of the call.



For more information on using this function, see <a href="/windows/desktop/api/objidl/nf-objidl-irunnableobject-lockrunning">IRunnableObject::LockRunning</a>.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-colockobjectexternal">CoLockObjectExternal</a>



<a href="/windows/desktop/api/objidl/nf-objidl-irunnableobject-lockrunning">IRunnableObject::LockRunning</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olenoteobjectvisible">OleNoteObjectVisible</a>
