---
UID: NN:faxcomex.IFaxConfiguration
title: IFaxConfiguration
author: windows-sdk-content
description: Defines various methods that provide configuration options for the fax service.
old-location: fax\_mfax_IFaxConfiguration.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxconfiguration\ifaxconfiguration.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxConfiguration, IFaxConfiguration interface [Fax Service], IFaxConfiguration interface [Fax Service],described, _mfax_IFaxConfiguration, fax._mfax_IFaxConfiguration, faxcomex/IFaxConfiguration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Faxcomex.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxConfiguration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxConfiguration interface


## -description


Defines various methods that provide configuration options for the fax service.
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxConfiguration</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxConfiguration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxConfiguration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f296407a-4f14-4532-841a-228b8d1db535">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04084c00-a025-423b-a49d-ed98fa1dc54b">Save</a>
</td>
<td align="left" width="63%">
Saves the object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxConfiguration</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d20f4793-9dc0-48a9-ba95-4f492d2752a7">AllowPersonalCoverPages</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates whether personal cover pages are allowed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2672f0e3-e412-4263-b3d1-b5b6c9cae708">ArchiveAgeLimit</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates how long a fax message is kept on the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c504b290-d970-4bc9-ae35-4b05b0d2be96">ArchiveLocation</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates the location of the archive on the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3386ec80-be4e-4105-ab57-dd634b57f67f">ArchiveSizeHigh</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The value that specifies the high-order 32-bit value (in bytes) for the size of the fax message archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e10cde26-deec-47b8-bc69-0b785087ab74">ArchiveSizeLow</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The value that specifies the low-order 32-bit value (in bytes) for the size of the fax message archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/02cfc898-b1c5-4647-81b0-1f34da6d2ce8">AutoCreateAccountOnConnect</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates whether the server automatically creates a fax account once a connection is initiated.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a6671e02-882c-41c0-828b-664464196958">Branding</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates whether the fax server generates a branding mark on outgoing faxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/718d3eea-0b6d-49c0-91c0-ca9d5a43ac1a">DiscountRateEnd</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates the time at which the discount rate period ends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/891175d4-90fc-479a-a0af-a17091c8ed2a">DiscountRateStart</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates the time at which the discount rate period begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2c896e7c-a110-4693-9e8d-4cbf6459c6e3">HighQuotaWaterMark</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates the maximum allotted size of a watermark.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f40268ab-6df0-4c4f-9c73-c3129be589cc">IncomingFaxesArePublic</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether incoming faxes are either viewable by everyone or private.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/939cf7c1-28dd-478a-910e-a5dd2192c0c8">LowQuotaWaterMark</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates the minimum size of a watermark.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3c94867a-5d20-4987-8b21-cae8317b4ff3">OutgoingQueueAgeLimit</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates the length of time that an undeliverable fax message is kept on the fax server before it is deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e81f9818-428f-457d-8362-bc73b95c990c">OutgoingQueueBlocked</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates whether the fax server queue for outgoing faxes has been blocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2c4e6dd9-d8c1-4e02-96df-8e8025be78aa">OutgoingQueuePaused</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates whether the outgoing queue has been paused.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4f5d647b-458e-418e-9534-065489266d16">Retries</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates the number of redial attempts for a given fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e6bb8e86-41bb-46a3-9a8a-a4b218439467">RetryDelay</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates the length of time the fax service should wait before retrying a failed fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/541abd86-8edb-4d52-a323-5bdafab24653">SizeQuotaWarning</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates whether the size quota warning is turned on.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6a59fa8d-b1fa-4629-9d75-fea38108f18c">UseArchive</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates whether faxes should be archived.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b7f26dc1-f183-411f-9693-274a61416982">UseDeviceTSID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates whether the TSID is used.
      

</td>
</tr>
</table> 


## -remarks



A default implementation of this interface is provided by the <a href="https://msdn.microsoft.com/381e098b-d130-4e15-9aba-cb0048cc5b98">FaxConfiguration</a> object.



