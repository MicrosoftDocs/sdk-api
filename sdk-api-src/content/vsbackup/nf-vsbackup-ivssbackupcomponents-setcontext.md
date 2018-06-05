---
UID: NF:vsbackup.IVssBackupComponents.SetContext
title: IVssBackupComponents::SetContext
author: windows-sdk-content
description: The SetContext method sets the context for subsequent shadow copy-related operations.
old-location: base\ivssbackupcomponents_setcontext.htm
old-project: VSS
ms.assetid: 0e466090-b551-44e8-a86d-75126352aa49
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssBackupComponents interface [VSS],SetContext method, IVssBackupComponents.SetContext, IVssBackupComponents::SetContext, SetContext, SetContext method [VSS], SetContext method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_setcontext, base.ivssbackupcomponents_setcontext, vsbackup/IVssBackupComponents::SetContext
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
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
-	IVssBackupComponents.SetContext
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssBackupComponents::SetContext


## -description



    The <b>SetContext</b> method sets the context 
    for subsequent shadow copy-related operations.
   


## -parameters




### -param lContext [in]


      The context to be set. The context must be one of the supported values of 
      <a href="https://msdn.microsoft.com/2efe3066-4b91-4501-bacb-4211b222e0c3">_VSS_SNAPSHOT_CONTEXT</a> or a supported bit mask (or
      bitwise OR) of 
      <a href="https://msdn.microsoft.com/0326a81e-036c-4548-9e09-29054e51fadd">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> with a 
      valid <b>_VSS_SNAPSHOT_CONTEXT</b>.
     


## -returns




      The default return value of this method is S_OK. The following are the valid return codes for this method.
     

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
Successfully set the context.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">

        The backup components object is not initialized, this method has been called during a restore operation, or 
        this method has not been called within the correct sequence.
       

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
</table>
 




## -remarks



The default context for VSS shadow copies is VSS_CTX_BACKUP.

<b>Windows XP:  </b>
     The only supported context is the default context, VSS_CTX_BACKUP. Therefore, calling 
     <b>SetContext</b> under Windows XP returns
     E_NOTIMPL.

<b>SetContext</b> can be called only once, 
    and it must be called prior to calling most VSS  functions.


    For details on how the context set by 
    <b>IVssBackupComponents::SetContext</b> affects 
    how a shadow copy is created and managed, see 
    <a href="https://msdn.microsoft.com/de5f1a5b-6e90-4abc-a232-aea93636772f">Implementation Details for 
    Creating Shadow Copies</a>.
   


    For a complete discussion of the permitted shadow copy contexts, see 
    <a href="https://msdn.microsoft.com/2efe3066-4b91-4501-bacb-4211b222e0c3">_VSS_SNAPSHOT_CONTEXT</a> and 
    <a href="https://msdn.microsoft.com/0326a81e-036c-4548-9e09-29054e51fadd">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a>.
   




## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/3cc6c375-8a24-4af3-b4ad-5a695cc2645c">IVssBackupComponents::DoSnapshotSet</a>



<a href="https://msdn.microsoft.com/6a0a6228-2131-48a6-8d18-9491969d265b">IVssBackupComponents::StartSnapshotSet</a>



<a href="https://msdn.microsoft.com/2efe3066-4b91-4501-bacb-4211b222e0c3">_VSS_SNAPSHOT_CONTEXT</a>



<a href="https://msdn.microsoft.com/0326a81e-036c-4548-9e09-29054e51fadd">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a>
 

 

