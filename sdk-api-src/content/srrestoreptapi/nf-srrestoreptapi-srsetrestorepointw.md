---
UID: NF:srrestoreptapi.SRSetRestorePointW
title: SRSetRestorePointW function (srrestoreptapi.h)
description: Specifies the beginning and the ending of a set of changes so that System Restore can create a restore point. (Unicode)
helpviewer_keywords: ["SRSetRestorePoint", "SRSetRestorePoint function [System Restore]", "SRSetRestorePointW", "_sr_srsetrestorepoint", "sr.srsetrestorepoint", "srrestoreptapi/SRSetRestorePoint", "srrestoreptapi/SRSetRestorePointW"]
old-location: sr\srsetrestorepoint.htm
tech.root: sr
ms.assetid: 46f0094d-9079-41b5-9efc-ef07082653d3
ms.date: 12/05/2018
ms.keywords: SRSetRestorePoint, SRSetRestorePoint function [System Restore], SRSetRestorePointA, SRSetRestorePointW, _sr_srsetrestorepoint, sr.srsetrestorepoint, srrestoreptapi/SRSetRestorePoint, srrestoreptapi/SRSetRestorePointA, srrestoreptapi/SRSetRestorePointW
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
req.lib: Sfc.Lib
req.dll: SrClient.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SRSetRestorePointW
 - srrestoreptapi/SRSetRestorePointW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - SrClient.dll
 - sfc.dll
api_name:
 - SRSetRestorePoint
 - SRSetRestorePointA
 - SRSetRestorePointW
---

# SRSetRestorePointW function


## -description

Specifies the beginning and the ending of a set of changes so that System Restore can create a restore point.

For a scriptable equivalent, see 
<a href="/windows/desktop/sr/createrestorepoint-systemrestore">CreateRestorePoint</a>.

## -parameters

### -param pRestorePtSpec [in]

A pointer to a 
<a href="/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa">RESTOREPOINTINFO</a> structure that specifies the restore point.

### -param pSMgrStatus [out]

A pointer to a 
<a href="/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-statemgrstatus">STATEMGRSTATUS</a> structure that receives the status information.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. The <b>llSequenceNumber</b> member of <i>pSMgrStatus</i> receives the sequence number of the restore point.

If the function fails, the return value is <b>FALSE</b>. The <b>nStatus</b> member of <i>pSMgrStatus</i> receives error information.

## -remarks

You must initialize COM security to allow NetworkService, LocalService and System to call back into any process that uses <b>SRSetRestorePoint</b>. This is necessary for <b>SRSetRestorePoint</b> to operate properly. For information on setting up the COM calls to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> and <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>, see <a href="/windows/desktop/sr/using-system-restore">Using System Restore</a>.

This function cannot be called in safe mode. It also fails if System Restore has been disabled (see 
<a href="/windows/desktop/sr/disable-systemrestore">Disable</a>).

When you call this function, System Restore takes a full snapshot of the registry and other system databases.

Applications should not call System Restore functions using load-time dynamic linking. Instead, use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function to load SrClient.dll and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to call the function.

Create restore points just prior to a system change, by calling 
<b>SRSetRestorePoint</b> with the <b>dwEventType</b> member of the 
<a href="/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa">RESTOREPOINTINFO</a> structure set to BEGIN_SYSTEM_CHANGE. After the changes to the system have been completed, call 
<b>SRSetRestorePoint</b> with <b>dwEventType</b> set to END_SYSTEM_CHANGE.

If the user cancels the application installation, the installer may remove the restore point it created when the installation began. Removing the restore point is optional and can prevent the user from recovering from unintentional changes made by the installer during the cancellation. If the installer is to remove a restore point, it can call the 
<a href="/windows/desktop/api/srrestoreptapi/nf-srrestoreptapi-srremoverestorepoint">SRRemoveRestorePoint</a> function, or call 
<b>SRSetRestorePoint</b> with <b>dwRestorePointType</b> set to CANCELLED_OPERATION, <b>dwEventType</b> set to END_SYSTEM_CHANGE, and <b>llSequenceNumber</b> set to the value returned by the initial call to <b>SRSetRestorePoint</b>.

Be careful when making nested calls to 
<b>SRSetRestorePoint</b>. For more information, see 
<a href="/windows/desktop/sr/nested-calls-to-srsetrestorepoint">Nested calls to SRSetRestorePoint</a>.


<b>Windows 8:  </b><p class="note">A new registry key enables application developers to change the frequency of restore-point creation. 

<p class="note">Applications should create this key to use it because it  will not preexist in the system. The following applies by default if the key does not exist. If an application calls the <b>SRSetRestorePoint</b> function to create a restore point, Windows skips creating this new restore point if any restore points have been created in the last 24 hours.   System Restore sets the <b>IISequenceNumber</b> member of the <a href="/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-statemgrstatus">STATEMGRSTATUS</a> structure to the sequence number for the restore point created previously in the day and sets the value of the <b>nStatus</b> member to <b>ERROR_SUCCESS</b>.

The <b>SRSetRestorePoint</b> function returns <b>TRUE</b>.

<p class="note">Developers can write applications that create the <b>DWORD</b> value <b>SystemRestorePointCreationFrequency</b> under the registry key <b>HKLM\Software\Microsoft\Windows NT\CurrentVersion\SystemRestore</b>. The value of this registry key can change the frequency of restore point creation.    

<p class="note">If the application calls <b>SRSetRestorePoint</b> to create a restore point, and the registry key value is 0, system restore does not skip creating the new restore point.  

<p class="note">If the application calls <b>SRSetRestorePoint</b> to create a restore point, and the registry key value is the integer N, system restore skips creating a new restore point if any restore points were created in the previous N minutes.






<b>Windows 8:  </b><p class="note">System Restore running on Windows 8 monitors files in the boot volume that are relevant for system restore only. Snapshots of the boot volume created by System Restore running on Windows 8 may be deleted if the snapshot is subsequently exposed by an earlier version of Windows.  Note that although there is only one system volume, there is one boot volume for each operating system in a multi-boot system. 

<p class="note">Developers can write applications that create the <b>DWORD</b> value <b>ScopeSnapshots</b> under the registry key <b>HKLM\Software\Microsoft\Windows NT\CurrentVersion\SystemRestore</b>. If this registry key value is 0, System Restore creates snapshots of the boot volume in the same way as in earlier versions of Windows.  If this value is deleted, System Restore running on Windows 8 resumes creating snapshots that monitor files in the boot volume that are relevant for system restore only. 






#### Examples

For an example, see <a href="/windows/desktop/sr/using-system-restore">Using System Restore</a>.

<div class="code"></div>




> [!NOTE]
> The srrestoreptapi.h header defines SRSetRestorePoint as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/srrestoreptapi/nf-srrestoreptapi-srremoverestorepoint">SRRemoveRestorePoint</a>
