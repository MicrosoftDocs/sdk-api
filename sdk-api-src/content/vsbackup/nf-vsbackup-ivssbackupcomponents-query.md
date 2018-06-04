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

# IVssBackupComponents::Query


## -description



    The <b>Query</b> method queries providers on the 
    system and/or the completed shadow copies in the system that reside in the current context. The method can be 
    called only during backup operations.
   


## -parameters




### -param QueriedObjectId [in]

Reserved. The value of this parameter must be GUID_NULL.


### -param eQueriedObjectType [in]


      Indicates restriction of the query to the given object type. A value of VSS_OBJECT_NONE indicates no 
      restriction—that is, all objects will be queried. 
      

Currently, the value of this parameter must be <b>VSS_OBJECT_NONE</b>.


### -param eReturnedObjectsType [in]


      Object types to be returned. The value of this parameter must be either 
      <b>VSS_OBJECT_SNAPSHOT</b> or <b>VSS_OBJECT_PROVIDER</b>.
     


### -param ppEnum [out]


      Doubly indirect pointer to an <a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a> enumerator object.
     


## -returns



The following are the valid return codes for this method.

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
        <a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a> interface.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller is not an administrator or a backup operator.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory or other system resources.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The queried object is not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">

        Expected provider error. The provider logged the error in the event log. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.
       

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

        Unexpected provider error. The error code is logged in the error log. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.
       

</td>
</tr>
</table>
 




## -remarks




    Because <b>Query</b> returns only information on 
    completed shadow copies, the only shadow copy state it can disclose is VSS_SS_COMPLETED.
   


    The method may be called only during backup operations and must be preceded by calls to 
    <a href="https://msdn.microsoft.com/df469964-c954-4f79-b88f-a521157a0c66">IVssBackupComponents::InitializeForBackup</a> 
    and <a href="https://msdn.microsoft.com/0e466090-b551-44e8-a86d-75126352aa49">IVssBackupComponents::SetContext</a>.
   


    While <b>Query</b> can return information on all of 
    the providers available on a system, it will return only information about shadow copies with the current context 
    (set by <a href="https://msdn.microsoft.com/0e466090-b551-44e8-a86d-75126352aa49">IVssBackupComponents::SetContext</a>). 
    For instance, if the <a href="https://msdn.microsoft.com/2efe3066-4b91-4501-bacb-4211b222e0c3">_VSS_SNAPSHOT_CONTEXT</a> context 
    is set to <b>VSS_CTX_BACKUP</b>, 
    <b>Query</b> will not return information on a shadow 
    copy created with a context of VSS_CTX_FILE_SHARE_BACKUP.
   


    While this method currently returns a lists of all available providers and/or all completed shadow copies, in the 
    future, specialized queries may be supported: for instance, querying all shadow copies associated with a provider.
   




## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/df469964-c954-4f79-b88f-a521157a0c66">IVssBackupComponents::InitializeForBackup</a>



<a href="https://msdn.microsoft.com/0e466090-b551-44e8-a86d-75126352aa49">IVssBackupComponents::SetContext</a>



<a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a>
 

 

