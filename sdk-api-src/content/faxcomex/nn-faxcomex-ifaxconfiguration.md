---
UID: NN:faxcomex.IFaxConfiguration
title: IFaxConfiguration (faxcomex.h)
author: windows-sdk-content
description: Defines various methods that provide configuration options for the fax service.
old-location: fax\_mfax_IFaxConfiguration.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxconfiguration\ifaxconfiguration.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxConfiguration, IFaxConfiguration interface [Fax Service], IFaxConfiguration interface [Fax Service],described, _mfax_IFaxConfiguration, fax._mfax_IFaxConfiguration, faxcomex/IFaxConfiguration
ms.topic: interface
f1_keywords: 
 - "faxcomex/IFaxConfiguration"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxConfiguration interface


## -description


Defines various methods that provide configuration options for the fax service.
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxConfiguration</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxConfiguration</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-refresh-vb">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-save-vb">Save</a>
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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-allowpersonalcoverpages-vb">AllowPersonalCoverPages</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-archiveagelimit-vb">ArchiveAgeLimit</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-archivelocation-vb">ArchiveLocation</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxconfiguration-get_archivesizehigh">ArchiveSizeHigh</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxconfiguration-get_archivesizelow">ArchiveSizeLow</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-autocreateaccountonconnect-vb">AutoCreateAccountOnConnect</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-branding-vb">Branding</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-discountrateend-vb">DiscountRateEnd</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-discountratestart-vb">DiscountRateStart</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-highquotawatermark-vb">HighQuotaWaterMark</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-incomingfaxesarepublic-vb">IncomingFaxesArePublic</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-lowquotawatermark-vb">LowQuotaWaterMark</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-outgoingqueueagelimit-vb">OutgoingQueueAgeLimit</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-blockoutgoingqueue-vb">OutgoingQueueBlocked</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-pauseoutgoingqueue-vb">OutgoingQueuePaused</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-retries-vb">Retries</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-retrydelay-vb">RetryDelay</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-sizequotawarning-vb">SizeQuotaWarning</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-usearchive-vb">UseArchive</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-usedevicetsid-vb">UseDeviceTSID</a>


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



A default implementation of this interface is provided by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration">FaxConfiguration</a> object.



