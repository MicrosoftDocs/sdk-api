---
UID: NF:wbemcli.IWbemBackupRestoreEx.Resume
title: IWbemBackupRestoreEx::Resume (wbemcli.h)
description: The IWbemBackUpRestoreEx::Resume method releases a lock on the Windows Management Instrumentation (WMI) repository so operations can continue.
helpviewer_keywords: ["IWbemBackupRestoreEx interface [Windows Management Instrumentation]","Resume method","IWbemBackupRestoreEx.Resume","IWbemBackupRestoreEx::Resume","Resume","Resume method [Windows Management Instrumentation]","Resume method [Windows Management Instrumentation]","IWbemBackupRestoreEx interface","wbemcli/IWbemBackupRestoreEx::Resume","wmi.iwbembackuprestoreex_resume"]
old-location: wmi\iwbembackuprestoreex_resume.htm
tech.root: wmi
ms.assetid: fa31860b-36f5-4182-a58c-b8747af0e628
ms.date: 12/05/2018
ms.keywords: IWbemBackupRestoreEx interface [Windows Management Instrumentation],Resume method, IWbemBackupRestoreEx.Resume, IWbemBackupRestoreEx::Resume, Resume, Resume method [Windows Management Instrumentation], Resume method [Windows Management Instrumentation],IWbemBackupRestoreEx interface, wbemcli/IWbemBackupRestoreEx::Resume, wmi.iwbembackuprestoreex_resume
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
 - IWbemBackupRestoreEx::Resume
 - wbemcli/IWbemBackupRestoreEx::Resume
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
 - IWbemBackupRestoreEx.Resume
---

# IWbemBackupRestoreEx::Resume


## -description

The <b>IWbemBackUpRestoreEx::Resume</b> method releases a lock on the Windows Management Instrumentation (WMI) repository so  operations can continue.



## -returns

This method returns an <b>HRESULT</b> that indicates the status of a method call. The following list lists the values contained within an <b>HRESULT</b>.

## -remarks

The <b>Resume</b> method should always be called when the <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbembackuprestoreex-pause">Pause</a> method is called. <b>Resume</b> must be called on the same instance of <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbembackuprestoreex">IWbemBackUpRestoreEx</a> that the <b>Pause</b> method is implemented. Releasing the object without calling <b>Resume</b> automatically causes the <b>Resume</b> method to be implemented.

<div class="alert"><b>Note</b>  To implement the <b>Resume</b> method, the client user must have <b>SE_BACKUP_NAME</b> prior to calling the method.</div>
<div> </div>

#### Examples

The following C++ example shows how to call the <b>IWbemBackUpRestoreEx::Resume</b> method.


```cpp
// The pInt variable is of type IWbemBackupRestoreEx*
pInt->Resume();
```

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbembackuprestoreex">IWbemBackupRestoreEx</a>
