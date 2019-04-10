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
---

# IWSManSession interface


## -description


Defines operations and session settings.  Any Windows Remote Management operations require creation of an <b>IWSManSession</b> object that connects to a remote computer, <a href="https://msdn.microsoft.com/en-us/library/Aa384465(v=VS.85).aspx">base management controller</a> (BMC), or the local computer. WinRM network operations include getting, writing, enumerating data, or invoking methods.  The methods of the <b>IWSManSession</b> object mirror the basic  operations defined in the WS-Management protocol.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSManSession</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSManSession</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7e8b561e-c724-427b-88a0-34a6c8a9c6bd">Create</a>
</td>
<td align="left" width="63%">
Creates a new instance of a resource and returns the URI of the new object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63674a3a-4819-4695-a8f5-648787d78cc4">Delete</a>
</td>
<td align="left" width="63%">
Deletes the resource specified in the resource URI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">Enumerate</a>
</td>
<td align="left" width="63%">
Enumerates a table, data collection, or  log resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6393cfb-0787-4d30-8d02-be0996885f22">Get</a>
</td>
<td align="left" width="63%">
Retrieves the resource specified by the  <a href="https://msdn.microsoft.com/en-us/library/Aa384465(v=VS.85).aspx">URI</a> and returns an XML representation of the current instance of the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3f4e33e-436b-4f05-8696-321a3bfbacd5">Identify</a>
</td>
<td align="left" width="63%">
Queries a remote computer to determine if it supports the WS-Management protocol

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3fdf769c-dc7e-4089-b781-be288855d5c1">Invoke</a>
</td>
<td align="left" width="63%">
Invokes a method and  returns the results of the method call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1224dab8-82d1-4416-8c21-e84fdda15deb">Put</a>
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

<a href="https://msdn.microsoft.com/883fc265-b84e-4757-a9b1-8c52174cb701">BatchItems</a>


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

<a href="https://msdn.microsoft.com/9fa89b5d-60c3-4a0d-9d4b-62a266e884aa">Error</a>


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

<a href="https://msdn.microsoft.com/23cec29b-20aa-440e-9c4d-c65cf81da719">Timeout</a>


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




<a href="https://msdn.microsoft.com/c996f074-f14b-4edd-80b7-8f4de4cbabb0">Windows Remote Management Reference</a>
 

 

