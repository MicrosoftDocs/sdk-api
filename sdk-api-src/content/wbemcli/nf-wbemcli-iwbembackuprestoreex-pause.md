---
UID: NF:wbemcli.IWbemBackupRestoreEx.Pause
title: IWbemBackupRestoreEx::Pause (wbemcli.h)
description: The IWbemBackupRestoreEx::Pause method locks out write operations from the Windows Management Instrumentation (WMI) repository, and may cause read operations to be blocked.
helpviewer_keywords: ["IWbemBackupRestoreEx interface [Windows Management Instrumentation]","Pause method","IWbemBackupRestoreEx.Pause","IWbemBackupRestoreEx::Pause","Pause","Pause method [Windows Management Instrumentation]","Pause method [Windows Management Instrumentation]","IWbemBackupRestoreEx interface","wbemcli/IWbemBackupRestoreEx::Pause","wmi.iwbembackuprestoreex_pause"]
old-location: wmi\iwbembackuprestoreex_pause.htm
tech.root: wmi
ms.assetid: ce4f2637-cf30-4087-bd49-b26554f434ca
ms.date: 12/05/2018
ms.keywords: IWbemBackupRestoreEx interface [Windows Management Instrumentation],Pause method, IWbemBackupRestoreEx.Pause, IWbemBackupRestoreEx::Pause, Pause, Pause method [Windows Management Instrumentation], Pause method [Windows Management Instrumentation],IWbemBackupRestoreEx interface, wbemcli/IWbemBackupRestoreEx::Pause, wmi.iwbembackuprestoreex_pause
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemBackupRestoreEx::Pause
 - wbemcli/IWbemBackupRestoreEx::Pause
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemBackupRestoreEx.Pause
---

# IWbemBackupRestoreEx::Pause


## -description

The <b>IWbemBackupRestoreEx::Pause</b> method locks out write operations from the Windows Management Instrumentation (WMI) repository, and may cause read operations to be blocked.



## -returns

This method returns an <b>HRESULT</b> that indicates the status of a method call. The following list lists the values contained within an <b>HRESULT</b>.

## -remarks

When implementing the <b>Pause</b> method, the <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbembackuprestoreex-resume">Resume</a> method should be called as soon as possible. If <b>Resume</b> is not called within fifteen (15) minutes, it is called automatically for you. Calling <b>Pause</b> two times on the same object without calling <b>Resume</b> first will fail. Calling <b>Pause</b> on two objects at the same time may cause the second object to lock up until <b>Resume</b> is called on the first object.

<div class="alert"><b>Note</b>  To implement the <b>Pause</b> method, the client user must have <b>SE_BACKUP_NAME</b> prior to calling the method.</div>
<div> </div>

#### Examples

The following C++ example shows how to correctly call the <b>IWbemBackupRestoreEx::Pause</b> method.


```cpp
// The pInt variable is of type IWbemBackupRestoreEx*
pInt->Pause();
```

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbembackuprestoreex">IWbemBackupRestoreEx</a>
