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

# IVssBackupComponents::EnableWriterClasses


## -description


The 
<b>EnableWriterClasses</b> method enables the specified writers to receive all events.


## -parameters




### -param rgWriterClassId [in]

An array containing one or more writer class identifiers.


### -param cClassId [in]

The number of entries in the <i>rgWriterClassId</i> array.


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
Successfully enabled the writer class.

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
The backup components object is not initialized, this method has been called during a restore operation, or this method has not been called within the correct sequence.

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



If the <b>EnableWriterClasses</b> method and the <a href="https://msdn.microsoft.com/7567bf23-4f4c-4210-87f7-4f90262fda7a">IVssBackupComponents::DisableWriterClasses</a> method are never called, all writer classes are enabled.

After the first call to <b>EnableWriterClasses</b> returns, the writer classes that were specified in the <i>rgWriterClassId</i> array are enabled, and all other writer classes are disabled. 

If you call <b>EnableWriterClasses</b> more than once, each call adds the writers in the <i>rgWriterClassId</i> array to the list of enabled writers.

If you call <b>EnableWriterClasses</b> one or more times and then call <a href="https://msdn.microsoft.com/7567bf23-4f4c-4210-87f7-4f90262fda7a">DisableWriterClasses</a>, the call to <b>DisableWriterClasses</b> disables any writers in the   <i>rgWriterClassId</i> array that were enabled in the calls to <b>EnableWriterClasses</b>.


    If you call <b>EnableWriterClasses</b>, you must do so before calling the <a href="https://msdn.microsoft.com/44f19c10-c966-4ab6-98dd-865d535955db">IVssBackupComponents::GatherWriterMetadata</a> method. If you call <b>GatherWriterMetadata</b> first and then call <b>EnableWriterClasses</b>, the call to <b>EnableWriterClasses</b> has no effect.  If you need to call <b>GatherWriterMetadata</b> first, to determine which writer classes to enable, you must call it from a different instance of the <a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/7567bf23-4f4c-4210-87f7-4f90262fda7a">IVssBackupComponents::DisableWriterClasses</a>



<a href="https://msdn.microsoft.com/746fb12d-83d7-463d-848d-36e095832d1a">IVssBackupComponents::DisableWriterInstances</a>
 

 

