---
UID: NN:dskquota.IDiskQuotaUser
title: IDiskQuotaUser (dskquota.h)
author: windows-sdk-content
description: Represents a single user quota entry in the volume quota information file.
old-location: fs\idiskquotauser.htm
tech.root: FileIO
ms.assetid: 27edbebc-35b4-4f6a-87cc-d8a99782f405
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDiskQuotaUser, IDiskQuotaUser interface [Files], IDiskQuotaUser interface [Files],described, _win32_idiskquotauser, base.idiskquotauser, dskquota/IDiskQuotaUser, fs.idiskquotauser
ms.topic: interface
f1_keywords: 
 - "dskquota/IDiskQuotaUser"
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
 - IDiskQuotaUser
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiskQuotaUser interface


## -description


Represents a single user quota entry in the volume quota information file. Through this 
    interface, you can query and modify user-specific quota information on an NTFS file system 
    volume. This interface is instantiated by using 
    <a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nn-dskquota-ienumdiskquotausers">IEnumDiskQuotaUsers</a>, 
    <a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-findusersid">IDiskQuotaControl::FindUserSid</a>, 
    <a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-findusername">IDiskQuotaControl::FindUserName</a>, 
    <a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-addusersid">IDiskQuotaControl::AddUserSid</a>, or 
    <a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-addusername">IDiskQuotaControl::AddUserName</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiskQuotaUser</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDiskQuotaUser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiskQuotaUser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getaccountstatus">GetAccountStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of the user object's account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getid">GetID</a>
</td>
<td align="left" width="63%">
Retrieves a unique identifier (ID) number for the DiskQuotaUser object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getname">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the name strings associated with a disk quota user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getquotainformation">GetQuotaInformation</a>
</td>
<td align="left" width="63%">
Retrieves the values for the user's warning threshold, hard quota limit, and quota used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getquotalimit">GetQuotaLimit</a>
</td>
<td align="left" width="63%">
Retrieves the user's quota limit value on the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getquotalimittext">GetQuotaLimitText</a>
</td>
<td align="left" width="63%">
Retrieves the user's quota limit for the volume. This limit is expressed as a text string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getquotathreshold">GetQuotaThreshold</a>
</td>
<td align="left" width="63%">
Retrieves the user's warning threshold value on the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getquotathresholdtext">GetQuotaThresholdText</a>
</td>
<td align="left" width="63%">
Retrieves the user's warning threshold for the volume. This threshold is expressed as a text string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getquotaused">GetQuotaUsed</a>
</td>
<td align="left" width="63%">
Retrieves the user's quota used value on the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getquotausedtext">GetQuotaUsedText</a>
</td>
<td align="left" width="63%">
Retrieves the user's quota used value for the volume. This value is expressed as a text string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getsid">GetSid</a>
</td>
<td align="left" width="63%">
Retrieves the user's security identifier (SID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getsidlength">GetSidLength</a>
</td>
<td align="left" width="63%">
Retrieves the length of the user's security identifier (SID), in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-invalidate">Invalidate</a>
</td>
<td align="left" width="63%">
Invalidates the quota information stored in the quota user object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-setquotalimit">SetQuotaLimit</a>
</td>
<td align="left" width="63%">
Sets the user's quota limit value on the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-setquotathreshold">SetQuotaThreshold</a>
</td>
<td align="left" width="63%">
Sets the user's warning threshold value on the volume.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>
 

 

