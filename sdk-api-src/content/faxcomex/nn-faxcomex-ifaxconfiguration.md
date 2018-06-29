---
UID: NN:faxcomex.IFaxConfiguration
title: IFaxConfiguration
author: windows-sdk-content
description: Defines various methods that provide configuration options for the fax service.
old-location: fax\_mfax_IFaxConfiguration.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxconfiguration\ifaxconfiguration.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxConfiguration interface


## -description


Defines various methods that provide configuration options for the fax service.
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxConfiguration</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxConfiguration</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/Aa358927(v=VS.85).aspx">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a>
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

<a href="https://msdn.microsoft.com/library/Aa358912(v=VS.85).aspx">AllowPersonalCoverPages</a>


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

<a href="https://msdn.microsoft.com/library/Aa358914(v=VS.85).aspx">ArchiveAgeLimit</a>


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

<a href="https://msdn.microsoft.com/library/Aa358915(v=VS.85).aspx">ArchiveLocation</a>


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

<a href="https://msdn.microsoft.com/library/Aa358916(v=VS.85).aspx">AutoCreateAccountOnConnect</a>


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

<a href="https://msdn.microsoft.com/library/Aa358919(v=VS.85).aspx">Branding</a>


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

<a href="https://msdn.microsoft.com/library/Aa358920(v=VS.85).aspx">DiscountRateEnd</a>


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

<a href="https://msdn.microsoft.com/library/Aa358921(v=VS.85).aspx">DiscountRateStart</a>


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

<a href="https://msdn.microsoft.com/library/Aa358922(v=VS.85).aspx">HighQuotaWaterMark</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn997390">IncomingFaxesArePublic</a>


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

<a href="https://msdn.microsoft.com/library/Aa358924(v=VS.85).aspx">LowQuotaWaterMark</a>


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

<a href="https://msdn.microsoft.com/library/Aa358925(v=VS.85).aspx">OutgoingQueueAgeLimit</a>


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

<a href="https://msdn.microsoft.com/library/Aa358918(v=VS.85).aspx">OutgoingQueueBlocked</a>


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

<a href="https://msdn.microsoft.com/library/Aa358926(v=VS.85).aspx">OutgoingQueuePaused</a>


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

<a href="https://msdn.microsoft.com/library/Aa358928(v=VS.85).aspx">Retries</a>


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

<a href="https://msdn.microsoft.com/library/Aa358932(v=VS.85).aspx">UseArchive</a>


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

<a href="https://msdn.microsoft.com/library/Aa358933(v=VS.85).aspx">UseDeviceTSID</a>


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



A default implementation of this interface is provided by the <a href="https://msdn.microsoft.com/library/Aa358913(v=VS.85).aspx">FaxConfiguration</a> object.



