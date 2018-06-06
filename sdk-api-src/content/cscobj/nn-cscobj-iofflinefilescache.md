---
UID: NN:cscobj.IOfflineFilesCache
title: IOfflineFilesCache
author: windows-sdk-content
description: Used to manage the Offline Files cache.
old-location: of\iofflinefilescache.htm
old-project: OfflineFiles
ms.assetid: 7b1b5ef6-355a-4760-9d54-ec73cc66fb8a
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IOfflineFilesCache, IOfflineFilesCache interface [Offline Files], IOfflineFilesCache interface [Offline Files],described, cscobj/IOfflineFilesCache, of.iofflinefilescache
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesCache
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesCache interface


## -description


Used to manage the Offline Files cache.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesCache</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOfflineFilesCache</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesCache</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6326364-fbd0-4446-97c3-6a3940856efb">DeleteItems</a>
</td>
<td align="left" width="63%">
Deletes files and directories from the local cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a187fd6b-0717-4663-b460-df96876cd9c3">DeleteItemsForUser</a>
</td>
<td align="left" width="63%">
Deletes a user's files and directories from the local cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7531018-4837-4fde-8947-0f099f6de9e5">Encrypt</a>
</td>
<td align="left" width="63%">
Encrypts or unencrypts the contents of the Offline Files cache cached for the calling user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f2bb562-810a-4cc1-a072-eb870149954a">EnumSettingObjects</a>
</td>
<td align="left" width="63%">
Creates an enumerator of instances of IOfflineFilesSetting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15696dbf-09a9-42e3-8400-20f7b9b171b7">FindItem</a>
</td>
<td align="left" width="63%">
Locates a particular file or directory item in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7a247c0-1bb2-40d5-8914-758c8f6c4c51">FindItemEx</a>
</td>
<td align="left" width="63%">
Locates a particular file or directory item in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94ea826a-bfc4-4010-a57f-c3a1af985d03">GetDiskSpaceInformation</a>
</td>
<td align="left" width="63%">
Retrieves the amount of disk space used by the Offline Files cache as well as the space limits applied to cache usage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87c2aced-84c9-40cb-bdf2-6974925e89d5">GetEncryptionStatus</a>
</td>
<td align="left" width="63%">
Retrieves the current encryption state (encrypted or unencrypted) of the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451128">GetLocation</a>
</td>
<td align="left" width="63%">
Retrieves the current fully qualified directory path of the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17b6572d-f05e-4f0e-a247-89acd2963d6b">GetSettingObject</a>
</td>
<td align="left" width="63%">
Creates an object that represents a particular Offline Files setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d9a2fda-baad-4ada-8a07-f39c9cfafdfa">IsPathCacheable</a>
</td>
<td align="left" width="63%">
Determines whether a specified UNC path is in the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6005d755-5e1b-4eba-95a2-b6c9c00b1a64">Pin</a>
</td>
<td align="left" width="63%">
Pins files, directories, and network shared folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25ee4586-3031-4815-9a35-ce57cf9366d7">ProcessAdminPinPolicy</a>
</td>
<td align="left" width="63%">
Causes Offline Files to process the "administratively assigned offline files" group policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/883f29cb-d551-4358-8e74-f901956d8829">RenameItem</a>
</td>
<td align="left" width="63%">
Renames a specified path in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdbfd5af-000a-4724-8a44-5641b2f75896">SetDiskSpaceLimits</a>
</td>
<td align="left" width="63%">
Sets disk space usage limits on the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a9dd105-ea68-40ce-b1cb-6126ca932095">Synchronize</a>
</td>
<td align="left" width="63%">
Synchronizes files and directories in the Offline Files cache with their corresponding copies in the applicable network shared folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32d81a75-8845-4bd5-a0ff-e056a06ac11c">Unpin</a>
</td>
<td align="left" width="63%">
Unpins files, directories, and network shared folders from the Offline Files cache.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

