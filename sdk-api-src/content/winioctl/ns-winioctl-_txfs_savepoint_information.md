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

# _TXFS_SAVEPOINT_INFORMATION structure


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

The 
    <b>FSCTL_TXFS_SAVEPOINT_INFORMATION</b> structure 
    specifies the action to perform, and on which transaction.


## -struct-fields




### -field KtmTransaction

Handle to the transaction on which to perform the savepoint operation.


### -field ActionCode

Specifies the savepoint action to perform. Valid values are:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXFS_SAVEPOINT_SET"></a><a id="txfs_savepoint_set"></a><dl>
<dt><b>TXFS_SAVEPOINT_SET</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Creates a new savepoint.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_SAVEPOINT_ROLLBACK"></a><a id="txfs_savepoint_rollback"></a><dl>
<dt><b>TXFS_SAVEPOINT_ROLLBACK</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
Rolls back to the savepoint specified by the <b>SavepointId</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_SAVEPOINT_CLEAR"></a><a id="txfs_savepoint_clear"></a><dl>
<dt><b>TXFS_SAVEPOINT_CLEAR</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
Clears the most recently set savepoint for the specified transaction.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_SAVEPOINT_CLEAR_ALL"></a><a id="txfs_savepoint_clear_all"></a><dl>
<dt><b>TXFS_SAVEPOINT_CLEAR_ALL</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">
Clears all savepoints for the transaction.

</td>
</tr>
</table>
 


### -field SavepointId

If <b>ActionCode</b> is <b>TXFS_SAVEPOINT_SET</b>, on output, 
      returns the newly-created savepoint ID.

If <b>ActionCode</b> is <b>TXFS_ROLLBACK_TO_SAVEPOINT</b>, on 
      input, specifies the savepoint ID to roll back to. Remains unchanged on output.

If <b>ActionCode</b> is <b>TXFS_SAVEPOINT_CLEAR</b> or 
      <b>TXFS_SAVEPOINT_CLEAR_ALL</b>, this member is not used; therefore, on input, specify 
      <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/50cf01b4-fd14-4468-9191-79ccd0e2bd05">FSCTL_TXFS_SAVEPOINT_INFORMATION</a>
 

 

