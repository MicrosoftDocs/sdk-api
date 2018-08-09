---
UID: NN:rend.ITDirectoryObjectConference
title: ITDirectoryObjectConference
author: windows-sdk-content
description: The ITDirectoryObjectConference interface provides methods that allow an application to set and get conference details. The ITDirectoryObjectConference interface is created by calling QueryInterface on ITDirectoryObject.
old-location: tapi3\itdirectoryobjectconference.htm
old-project: tapi
ms.assetid: bab167cf-2726-4423-87b3-69227404bddc
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITDirectoryObjectConference, ITDirectoryObjectConference interface [TAPI 2.2], ITDirectoryObjectConference interface [TAPI 2.2],described, _tapi3_itdirectoryobjectconference, rend/ITDirectoryObjectConference, tapi3.itdirectoryobjectconference
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: rend.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rend.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RND_ADVERTISING_SCOPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITDirectoryObjectConference
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: ADAM
---

# ITDirectoryObjectConference interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>ITDirectoryObjectConference</b> interface provides methods that allow an application to set and get conference details. The 
<b>ITDirectoryObjectConference</b> interface is created by calling <b>QueryInterface</b> on 
<a href="https://msdn.microsoft.com/a48644a4-43e2-4c52-84be-0cb5c49e6436">ITDirectoryObject</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITDirectoryObjectConference</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITDirectoryObjectConference</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITDirectoryObjectConference</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25e155ad-c809-4ff4-85cb-ca43cb203368">get_AdvertisingScope</a>
</td>
<td align="left" width="63%">
Gets advertising scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f90defa9-5e70-4168-9a07-ccb520bd5a1f">get_Description</a>
</td>
<td align="left" width="63%">
Gets description of conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3228efa-2501-44ec-ba85-0e3b7c00b483">get_IsEncrypted</a>
</td>
<td align="left" width="63%">
Gets whether conference is encrypted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b17be92c-eee6-43ec-bec0-75d4c30ad22f">get_Originator</a>
</td>
<td align="left" width="63%">
Gets conference originator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a9d1b8e-1ebc-4a67-87cf-f88aaf25c309">get_Protocol</a>
</td>
<td align="left" width="63%">
Gets protocol identification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aeb496d5-2cea-4c69-ba19-c9083d133c1e">get_StartTime</a>
</td>
<td align="left" width="63%">
Gets start time of conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df22b117-8382-4ea2-8e6b-961f87f41b21">get_StopTime</a>
</td>
<td align="left" width="63%">
Gets stop time of conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3ea4bfc-dcb6-46a1-83da-2d897487c2c1">get_Url</a>
</td>
<td align="left" width="63%">
Gets URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74d7c770-e11d-4d87-acdb-821d64feed0c">put_AdvertisingScope</a>
</td>
<td align="left" width="63%">
Sets advertising scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46f58067-22ec-490e-b6cc-0fdc12dbb8f7">put_Description</a>
</td>
<td align="left" width="63%">
Sets description of conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af2d55be-cd4f-498b-9c23-abb2dda39f6e">put_IsEncrypted</a>
</td>
<td align="left" width="63%">
Sets whether conference is encrypted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97e8b966-b65c-4c19-ac61-0b952657aec1">put_Originator</a>
</td>
<td align="left" width="63%">
Sets originator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87ccf59c-3fe6-4247-b7f9-d1fb8bcf4b69">put_StartTime</a>
</td>
<td align="left" width="63%">
Sets start time of conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2542f3e2-d391-4d96-8aa8-120d639f0468">put_StopTime</a>
</td>
<td align="left" width="63%">
Sets stop time of conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca275c06-fd8f-4044-b528-cc197e4f1177">put_Url</a>
</td>
<td align="left" width="63%">
Sets URL.

</td>
</tr>
</table> 

