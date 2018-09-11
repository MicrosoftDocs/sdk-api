---
UID: NN:faxcomex.IFaxOutgoingArchive
title: IFaxOutgoingArchive
author: windows-sdk-content
description: The IFaxOutgoingArchive interface describes a configuration object that is used by a fax client application to access and configure the archive of outbound fax messages transmitted successfully by the fax service.
old-location: fax\_mfax_faxoutgoingarchive_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_3wmd_cpp.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxOutgoingArchive, IFaxOutgoingArchive interface [Fax Service], IFaxOutgoingArchive interface [Fax Service],described, _mfax_faxoutgoingarchive_cpp, fax._mfax_faxoutgoingarchive_cpp, faxcomex/IFaxOutgoingArchive
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: faxcomex.h
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
 - IFaxOutgoingArchive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingArchive interface


## -description


The <b>IFaxOutgoingArchive</b> interface describes a configuration object that is used by a fax client application to access and configure the archive of outbound fax messages transmitted successfully by the fax service. You can also use the <b>IFaxOutgoingArchive</b> interface to retrieve a message from the archive using its message ID.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingArchive</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxOutgoingArchive</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxOutgoingArchive</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms689586(v=VS.85).aspx">GetMessage</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689586(v=VS.85).aspx">IFaxOutgoingArchive::GetMessage</a> method returns a fax message from the archive of outbound faxes by using the fax message ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms688294(v=VS.85).aspx">GetMessages</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688294(v=VS.85).aspx">IFaxOutgoingArchive::GetMessages</a> method returns a new iterator (archive cursor) for the archive of outbound fax messages. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690096(v=VS.85).aspx">IFaxOutgoingMessageIterator</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms689545(v=VS.85).aspx">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689545(v=VS.85).aspx">IFaxOutgoingArchive::Refresh</a> method refreshes <a href="https://msdn.microsoft.com/en-us/library/ms688634(v=VS.85).aspx">FaxOutgoingArchive</a> object information from the fax server. When the <b>IFaxOutgoingArchive::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/en-us/library/ms689213(v=VS.85).aspx">IFaxOutgoingArchive::Save</a> method call are lost.

<div class="alert"><b>Note</b>  In Windows Vista, Windows Server 2008, and later versions of Windows, this method is not supported and returns an error.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms689213(v=VS.85).aspx">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689213(v=VS.85).aspx">IFaxOutgoingArchive::Save</a> method saves the <a href="https://msdn.microsoft.com/en-us/library/ms688634(v=VS.85).aspx">FaxOutgoingArchive</a> object data.

<div class="alert"><b>Note</b>  In Windows Vista, Windows Server 2008, and later versions of Windows, this method is not supported and returns an error.</div>
<div> </div>
</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingArchive</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689532(v=VS.85).aspx">AgeLimit</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689532(v=VS.85).aspx">IFaxOutgoingArchive::get_AgeLimit</a> property is a value that indicates the number of days that the fax service retains fax messages in the archive of outbound faxes. The fax service deletes messages from the outbound archive when they exceed the age limit. If the value of this property is zero, the fax service does not enforce an age limit.

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/en-us/library/ms693549(v=VS.85).aspx">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/en-us/library/Aa358976(v=VS.85).aspx">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/en-us/library/Aa358914(v=VS.85).aspx">IFaxConfiguration::put_ArchiveAgeLimit</a>   or <a href="https://msdn.microsoft.com/en-us/library/Aa358914(v=VS.85).aspx">IFaxConfiguration::get_ArchiveAgeLimit</a> method.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689082(v=VS.85).aspx">ArchiveFolder</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689082(v=VS.85).aspx">IFaxOutgoingArchive::get_ArchiveFolder</a> property is a null-terminated string that specifies the folder location on the fax server for archived outbound faxes.

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/en-us/library/ms693549(v=VS.85).aspx">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/en-us/library/Aa358976(v=VS.85).aspx">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/en-us/library/Aa358915(v=VS.85).aspx">IFaxConfiguration::put_ArchiveLocation</a>   or <a href="https://msdn.microsoft.com/en-us/library/Aa358915(v=VS.85).aspx">IFaxConfiguration::get_ArchiveLocation</a> method.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689518(v=VS.85).aspx">HighQuotaWaterMark</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689518(v=VS.85).aspx">IFaxOutgoingArchive::get_HighQuotaWaterMark</a> property is a value that specifies the upper threshold for the size of the archive of inbound fax messages, in megabytes. If the archived fax messages in the archive exceed this value, and the <a href="https://msdn.microsoft.com/en-us/library/ms689560(v=VS.85).aspx">IFaxOutgoingArchive::get_SizeQuotaWarning</a> property is equal to <b>TRUE</b>, the fax service issues a warning in the event log.

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/en-us/library/ms693549(v=VS.85).aspx">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/en-us/library/Aa358976(v=VS.85).aspx">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/en-us/library/Aa358922(v=VS.85).aspx">IFaxConfiguration::put_HighQuotaWaterMark</a>   or <a href="https://msdn.microsoft.com/en-us/library/Aa358922(v=VS.85).aspx">IFaxConfiguration::get_HighQuotaWaterMark</a> method.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690239(v=VS.85).aspx">LowQuotaWaterMark</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690239(v=VS.85).aspx">IFaxOutgoingArchive::get_LowQuotaWaterMark</a> property is a value that specifies the lower threshold for the archive of outbound fax messages, in megabytes. If the fax service has issued a warning in the event log, the service does not issue additional warnings until the size of the outbound archive drops below this value.

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/en-us/library/ms693549(v=VS.85).aspx">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/en-us/library/Aa358976(v=VS.85).aspx">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/en-us/library/Aa358924(v=VS.85).aspx">IFaxConfiguration::put_LowQuotaWaterMark</a>   or <a href="https://msdn.microsoft.com/en-us/library/Aa358924(v=VS.85).aspx">IFaxConfiguration::get_LowQuotaWaterMark</a> method.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689112(v=VS.85).aspx">SizeHigh</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689112(v=VS.85).aspx">IFaxOutgoingArchive::get_SizeHigh</a> property is a value that specifies the high 32-bit value (in bytes) for the size of the archive of outgoing fax messages.

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/en-us/library/ms693549(v=VS.85).aspx">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/en-us/library/Aa358976(v=VS.85).aspx">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/3386ec80-be4e-4105-ab57-dd634b57f67f">IFaxConfiguration::get_ArchiveSizeHigh</a> method.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690155(v=VS.85).aspx">SizeLow</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690155(v=VS.85).aspx">IFaxOutgoingArchive::get_SizeLow</a> property is a value that specifies the low 32-bit value (in bytes) for the size of the archive of outgoing fax messages.

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/en-us/library/ms693549(v=VS.85).aspx">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/en-us/library/Aa358976(v=VS.85).aspx">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/e10cde26-deec-47b8-bc69-0b785087ab74">IFaxConfiguration::get_ArchiveSizeLow</a> method.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689560(v=VS.85).aspx">SizeQuotaWarning</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689560(v=VS.85).aspx">IFaxOutgoingArchive::get_SizeQuotaWarning</a> property is a Boolean value that indicates whether the fax service issues a warning in the event log when the size of the outbound archive exceeds the limit defined by the <a href="https://msdn.microsoft.com/en-us/library/ms689518(v=VS.85).aspx">IFaxOutgoingArchive::get_HighQuotaWaterMark</a> property.

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/en-us/library/ms693549(v=VS.85).aspx">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/en-us/library/Aa358976(v=VS.85).aspx">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/en-us/library/Aa358931(v=VS.85).aspx">IFaxConfiguration::put_SizeQuotaWarning</a>   or <a href="https://msdn.microsoft.com/en-us/library/Aa358931(v=VS.85).aspx">IFaxConfiguration::get_SizeQuotaWarning</a> method.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689119(v=VS.85).aspx">UseArchive</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689119(v=VS.85).aspx">IFaxOutgoingArchive::get_UseArchive</a> property is a Boolean value that indicates whether the fax service archives outbound fax messages. If this parameter is equal to <b>TRUE</b>, the fax service archives outbound fax messages. If this parameter is equal to <b>FALSE</b>, the fax service does not archive outbound faxes.

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/en-us/library/ms693549(v=VS.85).aspx">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/en-us/library/Aa358976(v=VS.85).aspx">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/en-us/library/Aa358932(v=VS.85).aspx">IFaxConfiguration::put_UseArchive</a>   or <a href="https://msdn.microsoft.com/en-us/library/Aa358932(v=VS.85).aspx">IFaxConfiguration::get_UseArchive</a> method.</div>
<div> </div>
</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutgoingArchive</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/ms688634(v=VS.85).aspx">FaxOutgoingArchive</a> object.



