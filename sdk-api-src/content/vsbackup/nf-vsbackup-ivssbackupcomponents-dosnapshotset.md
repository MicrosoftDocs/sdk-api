---
UID: NF:vsbackup.IVssBackupComponents.DoSnapshotSet
title: IVssBackupComponents::DoSnapshotSet method
author: windows-driver-content
description: Commits all shadow copies in this set simultaneously.
old-location: base\ivssbackupcomponents_dosnapshotset.htm
old-project: VSS
ms.assetid: 3cc6c375-8a24-4af3-b4ad-5a695cc2645c
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: DoSnapshotSet method [VSS], DoSnapshotSet method [VSS], IVssBackupComponents interface, DoSnapshotSet,IVssBackupComponents.DoSnapshotSet, IVssBackupComponents, IVssBackupComponents interface [VSS], DoSnapshotSet method, IVssBackupComponents::DoSnapshotSet, _win32_ivssbackupcomponents_dosnapshotset, base.ivssbackupcomponents_dosnapshotset, vsbackup/IVssBackupComponents::DoSnapshotSet
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
req.typenames: AMVPSIZE, *LPAMVPSIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssBackupComponents.DoSnapshotSet
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssBackupComponents::DoSnapshotSet method


## -description



    Commits all 
    shadow copies in this set simultaneously.
   


## -parameters




### -param ppAsync [out]

A
      doubly indirect pointer to the required <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> asynchronous 
      interface. This is used to query the method execution state and to retrieve the final error code.


## -returns




      The following are the valid return codes for this method. These error codes may be returned from this method, or 
      from the <a href="https://msdn.microsoft.com/85fb3ae8-dc09-4f6f-a96b-e4dc046ff48a">QueryStatus</a> method on the 
      <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface returned in the 
      <i>ppAsync</i> parameter.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">

        Successfully returned a pointer to an instance of the 
        <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface. See 
        <a href="https://msdn.microsoft.com/85fb3ae8-dc09-4f6f-a96b-e4dc046ff48a">IVssAsync::QueryStatus</a> for the valid values
        returned by the <i>pHrResult</i> parameter.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient backup privileges or is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppAsync</i>does not point to a valid pointer; that is, it is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">

        The backup components object has not been initialized or the prerequisite calls for a given shadow copy
        context have not been made prior to calling 
        <a href="https://msdn.microsoft.com/3cc6c375-8a24-4af3-b4ad-5a695cc2645c">DoSnapshotSet</a>.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INSUFFICIENT_STORAGE</b></dt>
</dl>
</td>
<td width="60%">

        The system or provider has insufficient storage space. If possible delete any old or unnecessary persistent 
        shadow copies and try again. This error code is only returned via the 
        <a href="https://msdn.microsoft.com/85fb3ae8-dc09-4f6f-a96b-e4dc046ff48a">QueryStatus</a> method on the 
        <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface returned in the 
        <i>ppAsync</i> parameter.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_FLUSH_WRITES_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">

        The system was unable to flush I/O writes. This can be a transient problem. It is recommended to wait ten 
        minutes and try again, up to three times.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_HOLD_WRITES_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">

        The system was unable to hold I/O writes. This can be a transient problem. It is recommended to wait ten 
        minutes and try again, up to three times.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_NESTED_VOLUME_LIMIT</b></dt>
</dl>
</td>
<td width="60%">
The specified volume is nested too deeply to participate in the VSS operation.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This return code is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">

        The provider was unable to perform the request at this time. This can be a transient problem. It is 
        recommended to wait ten minutes and try again, up to three times. This error code is only returned via the 
        <a href="https://msdn.microsoft.com/85fb3ae8-dc09-4f6f-a96b-e4dc046ff48a">QueryStatus</a> method on the 
        <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface returned in the 
        <i>ppAsync</i> parameter.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_REBOOT_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
The provider encountered an error that requires the user to restart the computer. 

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_TRANSACTION_FREEZE_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The system was unable to freeze the Distributed Transaction Coordinator (DTC) or the Kernel Transaction Manager (KTM).

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_TRANSACTION_THAW_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The system was unable to thaw the Distributed Transaction Coordinator (DTC) or the Kernel Transaction Manager (KTM).

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">

        Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED_PROVIDER_ERROR</b></dt>
</dl>
</td>
<td width="60%">

        The provider returned an unexpected error code. This can be a transient problem. It is recommended to wait 
        ten minutes and try again, up to three times. This error code is only returned via the 
        <a href="https://msdn.microsoft.com/85fb3ae8-dc09-4f6f-a96b-e4dc046ff48a">QueryStatus</a> method on the 
        <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface returned in the 
        <i>ppAsync</i> parameter.
       

</td>
</tr>
</table>
 




## -remarks




    The caller is responsible for releasing the 
    <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface.
   

This method cannot be called for a virtual hard disk (VHD) that is nested inside another VHD.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>VHDs are not supported.


    For information on how to use 
    <b>IVssBackupComponents::DoSnapshotSet</b> to
    create a standard backup shadow copy, see 
    <a href="https://msdn.microsoft.com/e6b082af-719b-4426-8217-0fc940f5884d">Overview of Pre-Backup Tasks</a> and 
    <a href="https://msdn.microsoft.com/a20570ea-e3eb-4d65-b8fa-9a27ce1a3e74">Simple Shadow Copy Creation for Backup</a>.
    For information on how the method is used under different VSS contexts, see 
    <a href="https://msdn.microsoft.com/de5f1a5b-6e90-4abc-a232-aea93636772f">Implementation Details for 
    Creating Shadow Copies</a>.
   




## -see-also




<a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a>



<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">IVssBackupComponents::AddComponent</a>



<a href="https://msdn.microsoft.com/6c20e386-7cd8-45d9-92d6-96d0a458db50">IVssBackupComponents::AddToSnapshotSet</a>



<a href="https://msdn.microsoft.com/46ce8282-a434-4b0b-b66e-40810052b34b">IVssBackupComponents::PrepareForBackup</a>



<a href="https://msdn.microsoft.com/6a0a6228-2131-48a6-8d18-9491969d265b">IVssBackupComponents::StartSnapshotSet</a>
 

 

