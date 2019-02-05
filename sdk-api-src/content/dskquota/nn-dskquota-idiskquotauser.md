---
UID: NN:dskquota.IDiskQuotaUser
title: IDiskQuotaUser
author: windows-sdk-content
description: Represents a single user quota entry in the volume quota information file.
old-location: fs\idiskquotauser.htm
tech.root: FileIO
ms.assetid: 27edbebc-35b4-4f6a-87cc-d8a99782f405
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiskQuotaUser, IDiskQuotaUser interface [Files], IDiskQuotaUser interface [Files],described, _win32_idiskquotauser, base.idiskquotauser, dskquota/IDiskQuotaUser, fs.idiskquotauser
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
 - IDiskQuotaUser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaUser interface


## -description


Represents a single user quota entry in the volume quota information file. Through this 
    interface, you can query and modify user-specific quota information on an NTFS file system 
    volume. This interface is instantiated by using 
    <a href="https://msdn.microsoft.com/f5916b17-66ed-46d4-87f1-5ee2ef57c1a1">IEnumDiskQuotaUsers</a>, 
    <a href="https://msdn.microsoft.com/a6ce8eb3-cfa3-43b4-80ee-6dbef41f99ac">IDiskQuotaControl::FindUserSid</a>, 
    <a href="https://msdn.microsoft.com/dae4e2d4-0293-4ee4-9687-9fed4b3a3600">IDiskQuotaControl::FindUserName</a>, 
    <a href="https://msdn.microsoft.com/a82b36a9-7270-4b4a-b850-67916864c052">IDiskQuotaControl::AddUserSid</a>, or 
    <a href="https://msdn.microsoft.com/306120e8-642a-439d-839c-944cb7fd7ee2">IDiskQuotaControl::AddUserName</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiskQuotaUser</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDiskQuotaUser</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d4027660-beb1-45eb-9dd3-f4c12df28051">GetAccountStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of the user object's account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04f84fd1-9ce4-4daa-91b3-24508f326f84">GetID</a>
</td>
<td align="left" width="63%">
Retrieves a unique identifier (ID) number for the DiskQuotaUser object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d47e064a-d121-41c3-b713-f81ff7052abf">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the name strings associated with a disk quota user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1640803-965a-473c-bf10-bee51d47fcfa">GetQuotaInformation</a>
</td>
<td align="left" width="63%">
Retrieves the values for the user's warning threshold, hard quota limit, and quota used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77b9099c-7696-47d8-ac08-b58a329909ee">GetQuotaLimit</a>
</td>
<td align="left" width="63%">
Retrieves the user's quota limit value on the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c200aae-dbc5-487c-a3a4-e8dcf50bc0f9">GetQuotaLimitText</a>
</td>
<td align="left" width="63%">
Retrieves the user's quota limit for the volume. This limit is expressed as a text string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58b925f3-b40a-4fab-86c6-725e04e6f721">GetQuotaThreshold</a>
</td>
<td align="left" width="63%">
Retrieves the user's warning threshold value on the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19391a9e-e64c-4e6f-8b52-efe59ed45ae5">GetQuotaThresholdText</a>
</td>
<td align="left" width="63%">
Retrieves the user's warning threshold for the volume. This threshold is expressed as a text string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3787648e-7788-4d09-a236-fe28a693a8ff">GetQuotaUsed</a>
</td>
<td align="left" width="63%">
Retrieves the user's quota used value on the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/401362a3-ee68-4af1-9ea5-c871c060ef33">GetQuotaUsedText</a>
</td>
<td align="left" width="63%">
Retrieves the user's quota used value for the volume. This value is expressed as a text string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1718b5eb-2385-4e0f-a6af-99a5ef73e55d">GetSid</a>
</td>
<td align="left" width="63%">
Retrieves the user's security identifier (SID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68fcb122-5d61-464a-99ae-d99e0d4a8117">GetSidLength</a>
</td>
<td align="left" width="63%">
Retrieves the length of the user's security identifier (SID), in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23a51df4-0578-43fe-99cd-491f709accab">Invalidate</a>
</td>
<td align="left" width="63%">
Invalidates the quota information stored in the quota user object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7c99415-685b-4a21-ac7b-68f4816aafb0">SetQuotaLimit</a>
</td>
<td align="left" width="63%">
Sets the user's quota limit value on the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c641a1c-fb04-4039-92bd-d3a1c7045355">SetQuotaThreshold</a>
</td>
<td align="left" width="63%">
Sets the user's warning threshold value on the volume.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>
 

 

