---
UID: NN:dskquota.IDiskQuotaControl
title: IDiskQuotaControl (dskquota.h)
description: Controls the disk quota facilities of a single NTFS file system volume.helpviewer_keywords: ["IDiskQuotaControl","IDiskQuotaControl interface [Files]","IDiskQuotaControl interface [Files]","described","_win32_idiskquotacontrol","base.idiskquotacontrol","dskquota/IDiskQuotaControl","fs.idiskquotacontrol"]
old-location: fs\idiskquotacontrol.htm
tech.root: FileIO
ms.assetid: fc9add5a-c9ef-462d-8125-128d48018717
ms.date: 12/05/2018
ms.keywords: IDiskQuotaControl, IDiskQuotaControl interface [Files], IDiskQuotaControl interface [Files],described, _win32_idiskquotacontrol, base.idiskquotacontrol, dskquota/IDiskQuotaControl, fs.idiskquotacontrol
f1_keywords:
- dskquota/IDiskQuotaControl
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiskQuotaControl interface


## -description


Controls the disk quota facilities of a single NTFS file system volume. The client can query and set volume-specific quota attributes through 
<b>IDiskQuotaControl</b>. The client can also enumerate all per-user quota entries on the volume. A client instantiates this interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function using the class identifier CLSID_DiskQuotaControl.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiskQuotaControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDiskQuotaControl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-addusername">AddUserName</a>
</td>
<td align="left" width="63%">
Adds a new quota entry on the volume for the specified user. The user is identified by domain and account name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-addusersid">AddUserSid</a>
</td>
<td align="left" width="63%">
Adds a new quota entry on the volume for the specified user. The user is identified by security identifier (SID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-createenumusers">CreateEnumUsers</a>
</td>
<td align="left" width="63%">
Creates an enumerator object for enumerating quota users on the volume. The newly created object implements the <a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nn-dskquota-ienumdiskquotausers">IEnumDiskQuotaUsers</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-createuserbatch">CreateUserBatch</a>
</td>
<td align="left" width="63%">
Creates a batching object for optimizing updates to the quota settings of multiple users simultaneously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-deleteuser">DeleteUser</a>
</td>
<td align="left" width="63%">
Removes a user entry from the volume quota information file, if the user's charged quota amount is zero (0) bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-findusername">FindUserName</a>
</td>
<td align="left" width="63%">
Locates a specific entry in the volume quota information. The user's account logon name is used as the search key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-findusersid">FindUserSid</a>
</td>
<td align="left" width="63%">
Locates a specific user entry in the volume quota information. The user's security identifier (SID) is used as the search key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-getdefaultquotalimit">GetDefaultQuotaLimit</a>
</td>
<td align="left" width="63%">
Retrieves the default quota limit for the volume. This limit is applied automatically to new users of the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-getdefaultquotalimittext">GetDefaultQuotaLimitText</a>
</td>
<td align="left" width="63%">
Retrieves the default quota limit for the volume. This limit is applied automatically to new users of the volume. The limit is expressed as a text string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-getdefaultquotathreshold">GetDefaultQuotaThreshold</a>
</td>
<td align="left" width="63%">
Retrieves the default quota warning threshold for the volume. This threshold is applied automatically to new users of the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-getdefaultquotathresholdtext">GetDefaultQuotaThresholdText</a>
</td>
<td align="left" width="63%">
Retrieves the default warning threshold for the volume. This threshold is expressed as a text string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-getquotalogflags">GetQuotaLogFlags</a>
</td>
<td align="left" width="63%">
Retrieves the flags that control the logging of user-related quota events on the volume. Logging makes an entry in the volume server's event log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-getquotastate">GetQuotaState</a>
</td>
<td align="left" width="63%">
Retrieves a set of flags describing the state of the quota system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-giveusernameresolutionpriority">GiveUserNameResolutionPriority</a>
</td>
<td align="left" width="63%">
Promotes the specified user object to the head of the queue so that it is next in line for resolution.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a new QuotaControl object by opening the NTFS file system volume with the requested access rights. The return value indicates whether the volume supports NTFS file system disk quotas and whether the caller has sufficient access rights.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-invalidatesidnamecache">InvalidateSidNameCache</a>
</td>
<td align="left" width="63%">
Invalidates the contents of the system's SID-to-name cache so that subsequent requests for new user objects (<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-ienumdiskquotausers-next">IEnumDiskQuotaUsers::Next</a>, <a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-findusersid">IDiskQuotaControl::FindUserSid</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-findusername">IDiskQuotaControl::FindUserName</a>) must obtain user names from the network domain controller. As names are obtained, they are cached.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-setdefaultquotalimit">SetDefaultQuotaLimit</a>
</td>
<td align="left" width="63%">
Modifies the default quota limit. This limit is applied automatically to new users of the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-setdefaultquotathreshold">SetDefaultQuotaThreshold</a>
</td>
<td align="left" width="63%">
Modifies the default warning threshold. This threshold is applied automatically to new users of the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-setquotalogflags">SetQuotaLogFlags</a>
</td>
<td align="left" width="63%">
Controls the logging of user-related quota events on the volume. Logging makes an entry in the volume server system's event log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-setquotastate">SetQuotaState</a>
</td>
<td align="left" width="63%">
Sets the state of the quota system. Not all state attributes can be modified. The enable, track, and enforce attributes can be modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-shutdownnameresolution">ShutdownNameResolution</a>
</td>
<td align="left" width="63%">
The SID-to-name resolver translates user security identifiers (SID) to user names. It runs as a background thread. When a quota control object is destroyed, this thread automatically terminates.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>
 

 

