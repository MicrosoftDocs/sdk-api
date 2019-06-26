---
UID: NN:wsmandisp.IWSManEnumerator
title: IWSManEnumerator (wsmandisp.h)
author: windows-sdk-content
description: Represents a stream of results returned from operations such as a WS-Management protocol WS-Enumeration:Enumerate operation.
old-location: winrm\iwsmanenumerator.htm
tech.root: winrm
ms.assetid: c7afac5d-946f-49ec-a7d0-de558ed2144b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSManEnumerator, IWSManEnumerator interface [Windows Remote Management], IWSManEnumerator interface [Windows Remote Management],described, winrm.iwsmanenumerator, wsmandisp/IWSManEnumerator
ms.topic: interface
f1_keywords: 
 - "wsmandisp/IWSManEnumerator"
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
 - IWSManEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSManEnumerator interface


## -description


Represents a stream of results returned from  operations such as a WS-Management protocol <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">WS-Enumeration</a>:Enumerate operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSManEnumerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSManEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWSManEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanenumerator-readitem">ReadItem</a>
</td>
<td align="left" width="63%">
Retrieves an item from the  resource and  returns an XML representation of the item.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSManEnumerator</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanenumerator-get_atendofstream">AtEndOfStream</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates that the end of items in the <b>IWSManEnumerator</b> object has been reached by calls to <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanenumerator-readitem">IWSManEnumerator::ReadItem</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanenumerator-get_error">Error</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an XML representation of additional error information.

</td>
</tr>
</table> 


## -remarks



The corresponding scripting object is <a href="https://docs.microsoft.com/windows/desktop/WinRM/enumerator">Enumerator</a>.

To limit the number of items that are read, set the <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-get_batchitems">IWSManSession::BatchItems</a> property.

Be aware that freeing the enumeration object clears pending enumeration requests.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-reference">Windows Remote Management Reference</a>
 

 

