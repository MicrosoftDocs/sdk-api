---
UID: NN:faxcomex.IFaxIncomingArchive
title: IFaxIncomingArchive (faxcomex.h)
author: windows-sdk-content
description: The IFaxIncomingArchive interface is used by a fax client application to access and configure the archive of inbound fax messages received successfully by the fax service.
old-location: fax\_mfax_faxincomingarchive_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_96jp_cpp.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxIncomingArchive, IFaxIncomingArchive interface [Fax Service], IFaxIncomingArchive interface [Fax Service],described, _mfax_faxincomingarchive_cpp, fax._mfax_faxincomingarchive_cpp, faxcomex/IFaxIncomingArchive
ms.topic: interface
f1_keywords: 
 - "faxcomex/IFaxIncomingArchive"
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
 - IFaxIncomingArchive
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxIncomingArchive interface


## -description


The <b>IFaxIncomingArchive</b> interface is used by a fax client application to access and configure the archive of inbound fax messages received successfully by the fax service. Use this interface to set and retrieve parameters related to configuring the archive of sent faxes. You can also use the <b>IFaxIncomingArchive</b> interface to retrieve a message from the archive by specifying its message ID.

A default implementation of <b>IFaxIncomingArchive</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive">FaxIncomingArchive</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingArchive</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxIncomingArchive</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxIncomingArchive</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-getmessage-vb">GetMessage</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-getmessage-vb">GetMessage</a> method returns a fax message from the archive of inbound faxes by using the fax message ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-getmessages-vb">GetMessages</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-getmessages-vb">GetMessages</a> method returns a new iterator (archive cursor) for the archive of inbound fax messages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-refresh-vb">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-refresh-vb">Refresh</a> method refreshes <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive">FaxIncomingArchive</a> object information from the fax server. When the <b>Refresh</b> method is called, any configuration changes made after the last <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-save-vb">Save</a> method call are lost.

<div class="alert"><b>Note</b>  In Windows Vista, Windows Server 2008, and later versions of Windows, this method is not supported and returns an error.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-save-vb">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-save-vb">Save</a> method saves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive">FaxIncomingArchive</a> object's data.

<div class="alert"><b>Note</b>  In Windows Vista, Windows Server 2008, and later versions of Windows, this method is not supported and returns an error.</div>
<div> </div>
</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingArchive</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-agelimit-vb">AgeLimit</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-agelimit-vb">AgeLimit</a> property is a value that indicates the number of days that the fax service retains fax messages in the archive of inbound faxes. The fax service deletes messages from the inbound archive when they exceed the age limit. If the value of this property is zero, the fax service does not enforce an age limit.

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-archiveagelimit-vb">IFaxConfiguration::put_ArchiveAgeLimit</a>   or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-archiveagelimit-vb">IFaxConfiguration::get_ArchiveAgeLimit</a> method.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-archivefolder-vb">ArchiveFolder</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-archivefolder-vb">ArchiveFolder</a> property is a null-terminated string that specifies the folder location on the fax server for archived inbound faxes.

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-archivelocation-vb">IFaxConfiguration::put_ArchiveLocation</a>   or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-archivelocation-vb">IFaxConfiguration::get_ArchiveLocation</a> method.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-highquotawatermark-vb">HighQuotaWaterMark</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-highquotawatermark-vb">HighQuotaWaterMark</a> property is a value that specifies the upper warning threshold for the size of the archive of inbound fax messages, in megabytes. If the size of the archive exceeds this value, and the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-sizequotawarning-vb">SizeQuotaWarning</a> property is equal to <b>TRUE</b>, the fax service issues a warning in the event log.

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-highquotawatermark-vb">IFaxConfiguration::put_HighQuotaWaterMark</a>   or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-highquotawatermark-vb">IFaxConfiguration::get_HighQuotaWaterMark</a> method.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-lowquotawatermark-vb">LowQuotaWaterMark</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-lowquotawatermark-vb">LowQuotaWaterMark</a> property is a value that specifies the lower warning threshold for the archive of inbound fax messages, in megabytes. If the fax service has issued a warning in the event log, the service does not issue additional warnings until the size of the inbound archive drops below this value.

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-lowquotawatermark-vb">IFaxConfiguration::put_LowQuotaWaterMark</a>   or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-lowquotawatermark-vb">IFaxConfiguration::get_LowQuotaWaterMark</a> method.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-sizehigh-vb">SizeHigh</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-sizehigh-vb">SizeHigh</a> property is a value that specifies the high 32-bit value (in bytes) for the size of the archive of inbound fax messages.

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-sizelow-vb">SizeLow</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-sizelow-vb">SizeLow</a> property is a value that specifies the low 32-bit value (in bytes) for the size of the archive of inbound fax messages.

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-sizequotawarning-vb">SizeQuotaWarning</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-sizequotawarning-vb">SizeQuotaWarning</a> property is a Boolean value that indicates whether the fax service issues a warning in the event log when the size of the inbound archive exceeds the limit defined by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-highquotawatermark-vb">HighQuotaWaterMark</a> property.

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-sizequotawarning-vb">IFaxConfiguration::put_SizeQuotaWarning</a>   or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-sizequotawarning-vb">IFaxConfiguration::get_SizeQuotaWarning</a> method.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-usearchive-vb">UseArchive</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-usearchive-vb">UseArchive</a> property is a Boolean value that indicates whether the fax service archives inbound fax messages. If this property is equal to <b>TRUE</b>, the fax service archives inbound fax messages. If this property is equal to <b>FALSE</b>, the fax service does not archive inbound faxes.

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-usearchive-vb">IFaxConfiguration::put_UseArchive</a>   or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-usearchive-vb">IFaxConfiguration::get_UseArchive</a> method.</div>
<div> </div>
</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive">FaxIncomingArchive</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

