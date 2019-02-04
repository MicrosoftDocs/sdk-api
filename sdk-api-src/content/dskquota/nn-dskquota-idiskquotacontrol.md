---
UID: NN:dskquota.IDiskQuotaControl
title: IDiskQuotaControl
author: windows-sdk-content
description: Controls the disk quota facilities of a single NTFS file system volume.
old-location: fs\idiskquotacontrol.htm
tech.root: FileIO
ms.assetid: fc9add5a-c9ef-462d-8125-128d48018717
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiskQuotaControl, IDiskQuotaControl interface [Files], IDiskQuotaControl interface [Files],described, _win32_idiskquotacontrol, base.idiskquotacontrol, dskquota/IDiskQuotaControl, fs.idiskquotacontrol
ms.topic: interface
req.header: dskquota.h
req.include-header: 
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
req.lib: 
req.dll: Dskquota.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dskquota.dll
api_name:
 - IDiskQuotaControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaControl interface


## -description


Controls the disk quota facilities of a single NTFS file system volume. The client can query and set volume-specific quota attributes through 
<b>IDiskQuotaControl</b>. The client can also enumerate all per-user quota entries on the volume. A client instantiates this interface by calling the <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function using the class identifier CLSID_DiskQuotaControl.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiskQuotaControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDiskQuotaControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiskQuotaControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/306120e8-642a-439d-839c-944cb7fd7ee2">AddUserName</a>
</td>
<td align="left" width="63%">
Adds a new quota entry on the volume for the specified user. The user is identified by domain and account name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a82b36a9-7270-4b4a-b850-67916864c052">AddUserSid</a>
</td>
<td align="left" width="63%">
Adds a new quota entry on the volume for the specified user. The user is identified by security identifier (SID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a29e1955-80e2-442d-9565-c885006be565">CreateEnumUsers</a>
</td>
<td align="left" width="63%">
Creates an enumerator object for enumerating quota users on the volume. The newly created object implements the <a href="https://msdn.microsoft.com/f5916b17-66ed-46d4-87f1-5ee2ef57c1a1">IEnumDiskQuotaUsers</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1c5a71f-4a2f-4bf9-b28f-11b87a558771">CreateUserBatch</a>
</td>
<td align="left" width="63%">
Creates a batching object for optimizing updates to the quota settings of multiple users simultaneously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7356f56-4cbb-40ed-9457-3818a3b47732">DeleteUser</a>
</td>
<td align="left" width="63%">
Removes a user entry from the volume quota information file, if the user's charged quota amount is zero (0) bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dae4e2d4-0293-4ee4-9687-9fed4b3a3600">FindUserName</a>
</td>
<td align="left" width="63%">
Locates a specific entry in the volume quota information. The user's account logon name is used as the search key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6ce8eb3-cfa3-43b4-80ee-6dbef41f99ac">FindUserSid</a>
</td>
<td align="left" width="63%">
Locates a specific user entry in the volume quota information. The user's security identifier (SID) is used as the search key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05af5869-0c77-4078-b6af-601a7df44244">GetDefaultQuotaLimit</a>
</td>
<td align="left" width="63%">
Retrieves the default quota limit for the volume. This limit is applied automatically to new users of the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a39d457c-9a6f-4d57-a91f-878fcb96916e">GetDefaultQuotaLimitText</a>
</td>
<td align="left" width="63%">
Retrieves the default quota limit for the volume. This limit is applied automatically to new users of the volume. The limit is expressed as a text string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e57ec1c0-cece-4379-a695-a33c832ea7af">GetDefaultQuotaThreshold</a>
</td>
<td align="left" width="63%">
Retrieves the default quota warning threshold for the volume. This threshold is applied automatically to new users of the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/faeb2fc5-92b0-49bf-a233-6b21683693bd">GetDefaultQuotaThresholdText</a>
</td>
<td align="left" width="63%">
Retrieves the default warning threshold for the volume. This threshold is expressed as a text string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79ba4f8a-9f89-4c15-9d17-b61960d12b62">GetQuotaLogFlags</a>
</td>
<td align="left" width="63%">
Retrieves the flags that control the logging of user-related quota events on the volume. Logging makes an entry in the volume server's event log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e35be3e-095a-4299-933d-6ebf3ccc5a1c">GetQuotaState</a>
</td>
<td align="left" width="63%">
Retrieves a set of flags describing the state of the quota system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07de4fc4-e68f-405d-bb96-14ccad37e8e8">GiveUserNameResolutionPriority</a>
</td>
<td align="left" width="63%">
Promotes the specified user object to the head of the queue so that it is next in line for resolution.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/352485fd-4ce7-435b-b8c2-81458786eb44">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a new QuotaControl object by opening the NTFS file system volume with the requested access rights. The return value indicates whether the volume supports NTFS file system disk quotas and whether the caller has sufficient access rights.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bca99e9-2dd7-4e79-ab6a-ad0e821dd9bf">InvalidateSidNameCache</a>
</td>
<td align="left" width="63%">
Invalidates the contents of the system's SID-to-name cache so that subsequent requests for new user objects (<a href="https://msdn.microsoft.com/498e7c21-b18a-4d43-bbe6-9f20c2e26221">IEnumDiskQuotaUsers::Next</a>, <a href="https://msdn.microsoft.com/a6ce8eb3-cfa3-43b4-80ee-6dbef41f99ac">IDiskQuotaControl::FindUserSid</a>, and <a href="https://msdn.microsoft.com/dae4e2d4-0293-4ee4-9687-9fed4b3a3600">IDiskQuotaControl::FindUserName</a>) must obtain user names from the network domain controller. As names are obtained, they are cached.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e4d8d04-dff2-477f-a5b2-8c8415cb3b52">SetDefaultQuotaLimit</a>
</td>
<td align="left" width="63%">
Modifies the default quota limit. This limit is applied automatically to new users of the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a935798b-91dc-4a36-aa31-7bde68b45778">SetDefaultQuotaThreshold</a>
</td>
<td align="left" width="63%">
Modifies the default warning threshold. This threshold is applied automatically to new users of the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e5a1637-ad10-4a36-8493-b57c254ae273">SetQuotaLogFlags</a>
</td>
<td align="left" width="63%">
Controls the logging of user-related quota events on the volume. Logging makes an entry in the volume server system's event log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bbacc3c-e212-4801-95d8-1e260123665d">SetQuotaState</a>
</td>
<td align="left" width="63%">
Sets the state of the quota system. Not all state attributes can be modified. The enable, track, and enforce attributes can be modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53a2dd49-46e8-4e84-bbc2-102a57f36abc">ShutdownNameResolution</a>
</td>
<td align="left" width="63%">
The SID-to-name resolver translates user security identifiers (SID) to user names. It runs as a background thread. When a quota control object is destroyed, this thread automatically terminates.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>
 

 

