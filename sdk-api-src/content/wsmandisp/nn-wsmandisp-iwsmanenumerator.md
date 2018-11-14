---
UID: NN:wsmandisp.IWSManEnumerator
title: IWSManEnumerator
author: windows-sdk-content
description: Represents a stream of results returned from operations such as a WS-Management protocol WS-Enumeration:Enumerate operation.
old-location: winrm\iwsmanenumerator.htm
tech.root: WinRM
ms.assetid: c7afac5d-946f-49ec-a7d0-de558ed2144b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWSManEnumerator, IWSManEnumerator interface [Windows Remote Management], IWSManEnumerator interface [Windows Remote Management],described, winrm.iwsmanenumerator, wsmandisp/IWSManEnumerator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
---

# IWSManEnumerator interface


## -description


Represents a stream of results returned from  operations such as a WS-Management protocol <a href="windows_remote_management_glossary.htm">WS-Enumeration</a>:Enumerate operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSManEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSManEnumerator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6b181a4b-347c-4874-969c-9ca7d36ec788">ReadItem</a>
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

<a href="https://msdn.microsoft.com/d80028b0-04ff-4c6d-90f5-1c81141a956c">AtEndOfStream</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates that the end of items in the <b>IWSManEnumerator</b> object has been reached by calls to <a href="https://msdn.microsoft.com/6b181a4b-347c-4874-969c-9ca7d36ec788">IWSManEnumerator::ReadItem</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/21157b6b-3cbd-4fe5-8df0-470b2a2c87d7">Error</a>


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



The corresponding scripting object is <a href="https://msdn.microsoft.com/8d8b461d-06a7-4600-8b68-2faf741a394b">Enumerator</a>.

To limit the number of items that are read, set the <a href="https://msdn.microsoft.com/883fc265-b84e-4757-a9b1-8c52174cb701">IWSManSession::BatchItems</a> property.

Be aware that freeing the enumeration object clears pending enumeration requests.




## -see-also




<a href="https://msdn.microsoft.com/c996f074-f14b-4edd-80b7-8f4de4cbabb0">Windows Remote Management Reference</a>
 

 

