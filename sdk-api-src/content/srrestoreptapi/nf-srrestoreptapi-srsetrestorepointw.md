---
UID: NF:srrestoreptapi.SRSetRestorePointW
title: SRSetRestorePointW function
author: windows-sdk-content
description: Specifies the beginning and the ending of a set of changes so that System Restore can create a restore point.
old-location: sr\srsetrestorepoint.htm
old-project: sr
ms.assetid: 46f0094d-9079-41b5-9efc-ef07082653d3
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: SRSetRestorePoint, SRSetRestorePoint function [System Restore], SRSetRestorePointA, SRSetRestorePointW, _sr_srsetrestorepoint, sr.srsetrestorepoint, srrestoreptapi/SRSetRestorePoint, srrestoreptapi/SRSetRestorePointA, srrestoreptapi/SRSetRestorePointW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: srrestoreptapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SRSetRestorePointW (Unicode) and SRSetRestorePointA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ENTERPRISE_DATA_POLICIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	SrClient.dll
-	sfc.dll
api_name:
-	SRSetRestorePoint
-	SRSetRestorePointA
-	SRSetRestorePointW
product: Windows
targetos: Windows
req.lib: 
req.dll: SrClient.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SRSetRestorePointW function


## -description


Specifies the beginning and the ending of a set of changes so that System Restore can create a restore point.

For a scriptable equivalent, see 
<a href="https://msdn.microsoft.com/30e1ff03-816c-463f-9f80-6d84149f0e0b">CreateRestorePoint</a>.


## -parameters




### -param pRestorePtSpec [in]

A pointer to a 
<a href="https://msdn.microsoft.com/6f3c1fab-5298-47bb-ba38-87d11f111245">RESTOREPOINTINFO</a> structure that specifies the restore point.


### -param pSMgrStatus [out]

A pointer to a 
<a href="https://msdn.microsoft.com/3531474b-1499-4c83-ab32-8c464c0eece0">STATEMGRSTATUS</a> structure that receives the status information.


## -returns



If the function succeeds, the return value is <b>TRUE</b>. The <b>llSequenceNumber</b> member of <i>pSMgrStatus</i> receives the sequence number of the restore point.

If the function fails, the return value is <b>FALSE</b>. The <b>nStatus</b> member of <i>pSMgrStatus</i> receives error information.




## -remarks



You must initialize COM security to allow NetworkService, LocalService and System to call back into any process that uses <b>SRSetRestorePoint</b>. This is necessary for <b>SRSetRestorePoint</b> to operate properly. For information on setting up the COM calls to <a href="_com_coinitializeex">CoInitializeEx</a> and <a href="_com_coinitializesecurity">CoInitializeSecurity</a>, see <a href="https://msdn.microsoft.com/98c79305-3659-4d1a-8165-bb6e451e2d1e">Using System Restore</a>.

This function cannot be called in safe mode. It also fails if System Restore has been disabled (see 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh450971">Disable</a>).

When you call this function, System Restore takes a full snapshot of the registry and other system databases.

Applications should not call System Restore functions using load-time dynamic linking. Instead, use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> function to load SrClient.dll and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to call the function.

Create restore points just prior to a system change, by calling 
<b>SRSetRestorePoint</b> with the <b>dwEventType</b> member of the 
<a href="https://msdn.microsoft.com/6f3c1fab-5298-47bb-ba38-87d11f111245">RESTOREPOINTINFO</a> structure set to BEGIN_SYSTEM_CHANGE. After the changes to the system have been completed, call 
<b>SRSetRestorePoint</b> with <b>dwEventType</b> set to END_SYSTEM_CHANGE.

If the user cancels the application installation, the installer may remove the restore point it created when the installation began. Removing the restore point is optional and can prevent the user from recovering from unintentional changes made by the installer during the cancellation. If the installer is to remove a restore point, it can call the 
<a href="https://msdn.microsoft.com/e0f27947-7d88-4d15-8a92-85f88c3b60d4">SRRemoveRestorePoint</a> function, or call 
<b>SRSetRestorePoint</b> with <b>dwRestorePointType</b> set to CANCELLED_OPERATION, <b>dwEventType</b> set to END_SYSTEM_CHANGE, and <b>llSequenceNumber</b> set to the value returned by the initial call to <b>SRSetRestorePoint</b>.

Be careful when making nested calls to 
<b>SRSetRestorePoint</b>. For more information, see 
<a href="https://msdn.microsoft.com/ee2dea47-f95d-4293-ac33-eff622b84db6">Nested calls to SRSetRestorePoint</a>.


<b>Windows 8:  </b><p class="note">A new registry key enables application developers to change the frequency of restore-point creation. 

<p class="note">Applications should create this key to use it because it  will not preexist in the system. The following applies by default if the key does not exist. If an application calls the <b>SRSetRestorePoint</b> function to create a restore point, Windows skips creating this new restore point if any restore points have been created in the last 24 hours.   System Restore sets the <b>IISequenceNumber</b> member of the <a href="https://msdn.microsoft.com/3531474b-1499-4c83-ab32-8c464c0eece0">STATEMGRSTATUS</a> structure to the sequence number for the restore point created previously in the day and sets the value of the <b>nStatus</b> member to <b>ERROR_SUCCESS</b>.

The <b>SRSetRestorePoint</b> function returns <b>TRUE</b>.

<p class="note">Developers can write applications that create the <b>DWORD</b> value <b>SystemRestorePointCreationFrequency</b> under the registry key <b>HKLM\Software\Microsoft\Windows NT\CurrentVersion\SystemRestore</b>. The value of this registry key can change the frequency of restore point creation.    

<p class="note">If the application calls <b>SRSetRestorePoint</b> to create a restore point, and the registry key value is 0, system restore does not skip creating the new restore point.  

<p class="note">If the application calls <b>SRSetRestorePoint</b> to create a restore point, and the registry key value is the integer N, system restore skips creating a new restore point if any restore points were created in the previous N minutes.






<b>Windows 8:  </b><p class="note">System Restore running on Windows 8 monitors files in the boot volume that are relevant for system restore only. Snapshots of the boot volume created by System Restore running on Windows 8 may be deleted if the snapshot is subsequently exposed by an earlier version of Windows.  Note that although there is only one system volume, there is one boot volume for each operating system in a multi-boot system. 

<p class="note">Developers can write applications that create the <b>DWORD</b> value <b>ScopeSnapshots</b> under the registry key <b>HKLM\Software\Microsoft\Windows NT\CurrentVersion\SystemRestore</b>. If this registry key value is 0, System Restore creates snapshots of the boot volume in the same way as in earlier versions of Windows.  If this value is deleted, System Restore running on Windows 8 resumes creating snapshots that monitor files in the boot volume that are relevant for system restore only. 






#### Examples

For an example, see <a href="https://msdn.microsoft.com/98c79305-3659-4d1a-8165-bb6e451e2d1e">Using System Restore</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e0f27947-7d88-4d15-8a92-85f88c3b60d4">SRRemoveRestorePoint</a>
 

 

