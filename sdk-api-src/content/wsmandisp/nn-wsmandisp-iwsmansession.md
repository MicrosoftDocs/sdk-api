---
UID: NN:wsmandisp.IWSManSession
title: IWSManSession (wsmandisp.h)
author: windows-sdk-content
description: Defines operations and session settings.
old-location: winrm\iwsmansession.htm
tech.root: winrm
ms.assetid: 3e016080-339f-4bda-bfd2-f912e090981f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSManSession, IWSManSession interface [Windows Remote Management], IWSManSession interface [Windows Remote Management],described, winrm.iwsmansession, wsmandisp/IWSManSession
ms.topic: interface
f1_keywords: 
 - "wsmandisp/IWSManSession"
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSManSession interface


## -description


Defines operations and session settings.  Any Windows Remote Management operations require creation of an <b>IWSManSession</b> object that connects to a remote computer, <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">base management controller</a> (BMC), or the local computer. WinRM network operations include getting, writing, enumerating data, or invoking methods.  The methods of the <b>IWSManSession</b> object mirror the basic  operations defined in the WS-Management protocol.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSManSession</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSManSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWSManSession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-create">Create</a>
</td>
<td align="left" width="63%">
Creates a new instance of a resource and returns the URI of the new object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes the resource specified in the resource URI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">Enumerate</a>
</td>
<td align="left" width="63%">
Enumerates a table, data collection, or  log resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-get">Get</a>
</td>
<td align="left" width="63%">
Retrieves the resource specified by the  <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">URI</a> and returns an XML representation of the current instance of the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-identify">Identify</a>
</td>
<td align="left" width="63%">
Queries a remote computer to determine if it supports the WS-Management protocol

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-invoke">Invoke</a>
</td>
<td align="left" width="63%">
Invokes a method and  returns the results of the method call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-put">Put</a>
</td>
<td align="left" width="63%">
Updates a resource.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSManSession</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-get_batchitems">BatchItems</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets and gets the number of   items in each enumeration batch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-get_error">Error</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets additional error information in an XML stream for the preceding call to an <b>IWSManSession</b> object method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-get_timeout">Timeout</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets and gets the maximum amount of time  (in milliseconds) that the client application waits for the WinRM to complete its operations.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-reference">Windows Remote Management Reference</a>
 

 

