---
UID: NN:cscobj.IOfflineFilesCache
title: IOfflineFilesCache
author: windows-sdk-content
description: Used to manage the Offline Files cache.
old-location: of\iofflinefilescache.htm
tech.root: OfflineFiles
ms.assetid: 7b1b5ef6-355a-4760-9d54-ec73cc66fb8a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IOfflineFilesCache, IOfflineFilesCache interface [Offline Files], IOfflineFilesCache interface [Offline Files],described, cscobj/IOfflineFilesCache, of.iofflinefilescache
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# IOfflineFilesCache interface


## -description


Used to manage the Offline Files cache.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesCache</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IOfflineFilesCache</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Bb530487(v=VS.85).aspx">DeleteItems</a>
</td>
<td align="left" width="63%">
Deletes files and directories from the local cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530488(v=VS.85).aspx">DeleteItemsForUser</a>
</td>
<td align="left" width="63%">
Deletes a user's files and directories from the local cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530489(v=VS.85).aspx">Encrypt</a>
</td>
<td align="left" width="63%">
Encrypts or unencrypts the contents of the Offline Files cache cached for the calling user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530490(v=VS.85).aspx">EnumSettingObjects</a>
</td>
<td align="left" width="63%">
Creates an enumerator of instances of IOfflineFilesSetting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530491(v=VS.85).aspx">FindItem</a>
</td>
<td align="left" width="63%">
Locates a particular file or directory item in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530492(v=VS.85).aspx">FindItemEx</a>
</td>
<td align="left" width="63%">
Locates a particular file or directory item in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530493(v=VS.85).aspx">GetDiskSpaceInformation</a>
</td>
<td align="left" width="63%">
Retrieves the amount of disk space used by the Offline Files cache as well as the space limits applied to cache usage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530494(v=VS.85).aspx">GetEncryptionStatus</a>
</td>
<td align="left" width="63%">
Retrieves the current encryption state (encrypted or unencrypted) of the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530495(v=VS.85).aspx">GetLocation</a>
</td>
<td align="left" width="63%">
Retrieves the current fully qualified directory path of the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530496(v=VS.85).aspx">GetSettingObject</a>
</td>
<td align="left" width="63%">
Creates an object that represents a particular Offline Files setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530497(v=VS.85).aspx">IsPathCacheable</a>
</td>
<td align="left" width="63%">
Determines whether a specified UNC path is in the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530498(v=VS.85).aspx">Pin</a>
</td>
<td align="left" width="63%">
Pins files, directories, and network shared folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530499(v=VS.85).aspx">ProcessAdminPinPolicy</a>
</td>
<td align="left" width="63%">
Causes Offline Files to process the "administratively assigned offline files" group policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530500(v=VS.85).aspx">RenameItem</a>
</td>
<td align="left" width="63%">
Renames a specified path in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530501(v=VS.85).aspx">SetDiskSpaceLimits</a>
</td>
<td align="left" width="63%">
Sets disk space usage limits on the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530502(v=VS.85).aspx">Synchronize</a>
</td>
<td align="left" width="63%">
Synchronizes files and directories in the Offline Files cache with their corresponding copies in the applicable network shared folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530503(v=VS.85).aspx">Unpin</a>
</td>
<td align="left" width="63%">
Unpins files, directories, and network shared folders from the Offline Files cache.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530659(v=VS.85).aspx">Offline Files API Interfaces</a>
 

 

