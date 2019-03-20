---
UID: NL:vswriter.IVssComponentEx
title: IVssComponentEx (vswriter.h)
author: windows-sdk-content
description: Defines additional methods for examining and modifying information about components contained in a requester's Backup Components Document.
old-location: base\ivsscomponentex.htm
tech.root: VSS
ms.assetid: b11f65b0-2de2-478b-88b6-4696a8da2419
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVssComponentEx, IVssComponentEx interface, IVssComponentEx interface,described, base.ivsscomponentex, vswriter/IVssComponentEx
ms.topic: class
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssComponentEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssComponentEx class


## -description


Defines additional methods for examining  and modifying information about components contained in a requester's Backup 
    Components Document.

The <b>IVssComponentEx</b> interface is a C++ (not COM) interface.

To obtain an instance of the <b>IVssComponentEx</b> 
   interface, call the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> method of the 
   <a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a> interface, and pass 
   the <b>IID_IVssComponentEx</b> constant as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssComponentEx</b> interface inherits from <a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>. <b>IVssComponentEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssComponentEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca85cf27-b16c-4356-abb8-eb6474db637f">GetAuthoritativeRestore</a>
</td>
<td align="left" width="63%">
Determines whether a requester has marked the restore of a component as authoritative for a replicated data store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51f96d3e-c783-42f4-9e04-94bf3a6b7c09">GetPostSnapshotFailureMsg</a>
</td>
<td align="left" width="63%">
Returns the <a href="https://msdn.microsoft.com/en-us/library/Aa384664(v=VS.85).aspx">PostSnapshot</a> failure message string that a writer has  set for a given component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b086ff8d-ff51-4550-887d-e7741e2469f2">GetPrepareForBackupFailureMsg</a>
</td>
<td align="left" width="63%">
Returns the <a href="https://msdn.microsoft.com/en-us/library/Aa384664(v=VS.85).aspx">PrepareForBackup</a> failure message string that a writer has  set for a given component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a544bcc1-6a42-4cda-824c-2b027b8a4a6f">GetRestoreName</a>
</td>
<td align="left" width="63%">
Obtains the logical name assigned to a component that is being restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ba52c80-2229-4653-bd5b-85d9f11cd127">GetRollForward</a>
</td>
<td align="left" width="63%">
Obtains the roll-forward operation type for a component and obtains the restore point for a partial roll-forward operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cf4e512-d557-4187-b489-5cca76c0560f">SetPostSnapshotFailureMsg</a>
</td>
<td align="left" width="63%">
Sets a <a href="https://msdn.microsoft.com/en-us/library/Aa384664(v=VS.85).aspx">PostSnapshot</a> failure message string for a component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2c48c06-8bfc-431b-aab3-89ec9b30a9a0">SetPrepareForBackupFailureMsg</a>
</td>
<td align="left" width="63%">
Sets a <a href="https://msdn.microsoft.com/en-us/library/Aa384664(v=VS.85).aspx">PrepareForBackup</a> failure message string for a component.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>
 

 

