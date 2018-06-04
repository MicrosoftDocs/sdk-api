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

# _TXFS_GET_TRANSACTED_VERSION structure


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Contains the information about the base and latest versions of the specified file.


## -struct-fields




### -field ThisBaseVersion

The version of the file that this handle is opened with. This member can be one of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXFS_TRANSACTED_VERSION_NONTRANSACTED"></a><a id="txfs_transacted_version_nontransacted"></a><dl>
<dt><b>TXFS_TRANSACTED_VERSION_NONTRANSACTED</b></dt>
<dt>0xFFFFFFFE</dt>
</dl>
</td>
<td width="60%">
The file is not a transacted file.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_TRANSACTED_VERSION_UNCOMMITTED"></a><a id="txfs_transacted_version_uncommitted"></a><dl>
<dt><b>TXFS_TRANSACTED_VERSION_UNCOMMITTED</b></dt>
<dt>0xFFFFFFFF</dt>
</dl>
</td>
<td width="60%">
The file has been opened as a transacted writer.

</td>
</tr>
</table>
 

If the handle has been opened as a transacted reader, the value returned for this member is a positive 
      integer that represents the version number of the file the handle is associated with.


### -field LatestVersion

The most recently committed version of the file.


### -field ThisMiniVersion

If the handle to a miniversion is open, this member contains the ID of the miniversion. If the handle is 
      not open, this member is zero (0).


### -field FirstMiniVersion

 The first available miniversion for this file. If there are no miniversions, or they are not visible to 
      the transaction bound to the file handle, this field is zero (0).


### -field LatestMiniVersion

The latest available miniversion for this file. If there are no miniversions, or they are not visible to 
      the transaction bound to the file handle, this field is zero (0).


## -remarks



The base version number remains the same for the lifetime of a handle. The latest version number increases as 
    long as a handle is still open to a file and a change is committed.  When the handle is closed, the version number 
    is reset to zero.




## -see-also




<a href="https://msdn.microsoft.com/71864348-1266-4ac5-a4b5-b9aaff52b0c5">FSCTL_TXFS_GET_TRANSACTED_VERSION</a>
 

 

