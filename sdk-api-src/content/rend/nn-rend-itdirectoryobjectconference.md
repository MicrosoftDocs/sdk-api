---
UID: NN:rend.ITDirectoryObjectConference
title: ITDirectoryObjectConference (rend.h)
author: windows-sdk-content
description: The ITDirectoryObjectConference interface provides methods that allow an application to set and get conference details. The ITDirectoryObjectConference interface is created by calling QueryInterface on ITDirectoryObject.
old-location: tapi3\itdirectoryobjectconference.htm
tech.root: Tapi
ms.assetid: bab167cf-2726-4423-87b3-69227404bddc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITDirectoryObjectConference, ITDirectoryObjectConference interface [TAPI 2.2], ITDirectoryObjectConference interface [TAPI 2.2],described, _tapi3_itdirectoryobjectconference, rend/ITDirectoryObjectConference, tapi3.itdirectoryobjectconference
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
req.lib: 
req.dll: Rend.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITDirectoryObjectConference interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>ITDirectoryObjectConference</b> interface provides methods that allow an application to set and get conference details. The 
<b>ITDirectoryObjectConference</b> interface is created by calling <b>QueryInterface</b> on 
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITDirectoryObjectConference</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITDirectoryObjectConference</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-get_advertisingscope">get_AdvertisingScope</a>
</td>
<td align="left" width="63%">
Gets advertising scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-get_description">get_Description</a>
</td>
<td align="left" width="63%">
Gets description of conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-get_isencrypted">get_IsEncrypted</a>
</td>
<td align="left" width="63%">
Gets whether conference is encrypted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-get_originator">get_Originator</a>
</td>
<td align="left" width="63%">
Gets conference originator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-get_protocol">get_Protocol</a>
</td>
<td align="left" width="63%">
Gets protocol identification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-get_starttime">get_StartTime</a>
</td>
<td align="left" width="63%">
Gets start time of conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-get_stoptime">get_StopTime</a>
</td>
<td align="left" width="63%">
Gets stop time of conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-get_url">get_Url</a>
</td>
<td align="left" width="63%">
Gets URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-put_advertisingscope">put_AdvertisingScope</a>
</td>
<td align="left" width="63%">
Sets advertising scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-put_description">put_Description</a>
</td>
<td align="left" width="63%">
Sets description of conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-put_isencrypted">put_IsEncrypted</a>
</td>
<td align="left" width="63%">
Sets whether conference is encrypted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-put_originator">put_Originator</a>
</td>
<td align="left" width="63%">
Sets originator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-put_starttime">put_StartTime</a>
</td>
<td align="left" width="63%">
Sets start time of conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-put_stoptime">put_StopTime</a>
</td>
<td align="left" width="63%">
Sets stop time of conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-put_url">put_Url</a>
</td>
<td align="left" width="63%">
Sets URL.

</td>
</tr>
</table> 

