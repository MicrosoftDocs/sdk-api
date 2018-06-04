---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MsiEndTransaction function


## -description


The  <b>MsiEndTransaction</b> function can commit or roll back all the installations belonging to the transaction opened by the <a href="https://msdn.microsoft.com/05904e58-b24d-4d2c-8b59-a66ad71b494a">MsiBeginTransaction</a> function. This function should be called by the current owner of the transaction. 

<b><a href="https://msdn.microsoft.com/7256b759-3fb5-4195-b0e4-a1631327ebb7">Windows Installer 4.0 and earlier</a>:  </b>Not supported. This function is available beginning with Windows Installer 4.5.


## -parameters




### -param dwTransactionState [in]

The value of this parameter determines whether the installer commits or rolls back all the installations belonging to the transaction. The value can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>MSITRANSACTIONSTATE_ROLLBACK</dt>
</dl>
</td>
<td width="60%">
Performs a <a href="https://msdn.microsoft.com/6c70e788-beb0-46db-94b0-1bbaac972acf">Rollback Installation</a> to undo changes to the system belonging to the transaction opened by the <a href="https://msdn.microsoft.com/05904e58-b24d-4d2c-8b59-a66ad71b494a">MsiBeginTransaction</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>MSITRANSACTIONSTATE_COMMIT</dt>
</dl>
</td>
<td width="60%">
Commits all changes to the system belonging to the transaction. Runs any <a href="https://msdn.microsoft.com/ad766585-e8ac-44b6-9717-7979f803886c">Commit Custom Actions</a> and commits to the system any changes to Win32 or common language runtime assemblies. Deletes the rollback script, and after using this option, the transaction's changes can no longer be undone with a  <a href="https://msdn.microsoft.com/6c70e788-beb0-46db-94b0-1bbaac972acf">Rollback Installation</a>.  

</td>
</tr>
</table>
 


## -returns



The <b>MsiEndTransaction</b> function returns the following values.
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
A transaction can be ended only by the current owner.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
An installation belonging to the transaction could not be completed. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_ALREADY_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
An installation belonging to the transaction is still in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ROLLBACK_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
An installation belonging to the transaction did not complete. During the installation, the <a href="https://msdn.microsoft.com/5510b393-1f2e-44ba-97f5-663674d55b20">DisableRollback</a> action disabled <a href="https://msdn.microsoft.com/6c70e788-beb0-46db-94b0-1bbaac972acf">rollback installations</a> of the package. The installer rolls back the installation up to the point where rollback was disabled, and the function returns this error.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c4a0f4d8-818d-4e60-908b-adaa2a54de95">Multiple Package Installations</a>
 

 

