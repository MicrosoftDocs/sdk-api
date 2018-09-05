---
UID: NF:wbemcli.IWbemBackupRestoreEx.Resume
title: IWbemBackupRestoreEx::Resume
author: windows-sdk-content
description: The IWbemBackUpRestoreEx::Resume method releases a lock on the Windows Management Instrumentation (WMI) repository so operations can continue.
old-location: wmi\iwbembackuprestoreex_resume.htm
old-project: WmiSdk
ms.assetid: fa31860b-36f5-4182-a58c-b8747af0e628
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: IWbemBackupRestoreEx interface [Windows Management Instrumentation],Resume method, IWbemBackupRestoreEx.Resume, IWbemBackupRestoreEx::Resume, Resume, Resume method [Windows Management Instrumentation], Resume method [Windows Management Instrumentation],IWbemBackupRestoreEx interface, wbemcli/IWbemBackupRestoreEx::Resume, wmi.iwbembackuprestoreex_resume
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.redist: 
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
tech.root: 
req.typenames: WMI_OBJ_TEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemBackupRestoreEx.Resume
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemBackupRestoreEx::Resume


## -description


The <b>IWbemBackUpRestoreEx::Resume</b> method releases a lock on the Windows Management Instrumentation (WMI) repository so  operations can continue.


## -parameters






## -returns



This method returns an <b>HRESULT</b> that indicates the status of a method call. The following list lists the values contained within an <b>HRESULT</b>.




## -remarks



The <b>Resume</b> method should always be called when the <a href="https://msdn.microsoft.com/ce4f2637-cf30-4087-bd49-b26554f434ca">Pause</a> method is called. <b>Resume</b> must be called on the same instance of <a href="https://msdn.microsoft.com/5349359a-e15f-4799-abad-f4a5fc3e89ea">IWbemBackUpRestoreEx</a> that the <b>Pause</b> method is implemented. Releasing the object without calling <b>Resume</b> automatically causes the <b>Resume</b> method to be implemented.

<div class="alert"><b>Note</b>  To implement the <b>Resume</b> method, the client user must have <b>SE_BACKUP_NAME</b> prior to calling the method.</div>
<div> </div>

#### Examples

The following C++ example shows how to call the <b>IWbemBackUpRestoreEx::Resume</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// The pInt variable is of type IWbemBackupRestoreEx*
pInt-&gt;Resume();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5349359a-e15f-4799-abad-f4a5fc3e89ea">IWbemBackupRestoreEx</a>
 

 

