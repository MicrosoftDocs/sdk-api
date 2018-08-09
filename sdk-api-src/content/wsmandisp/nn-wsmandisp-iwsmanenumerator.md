---
UID: NN:wsmandisp.IWSManEnumerator
title: IWSManEnumerator
author: windows-sdk-content
description: Represents a stream of results returned from operations, such as a Pull operation.
old-location: winrm\enumerator.htm
old-project: winrm
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Enumerator, Enumerator object [Windows Remote Management], Enumerator object [Windows Remote Management],described, IWSManEnumerator, winrm.enumerator, wsman.enumerator, wsmandisp/Enumerator
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WSManProxyAuthenticationFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - Enumerator
 - IWSManEnumerator
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManEnumerator interface


## -description


Represents a stream of results returned from operations, such as a Pull operation. For example, the <a href="https://msdn.microsoft.com/ed8ad3ad-d033-45cb-b681-995c5f73b12e">Session.Enumerate</a> method returns multiple results.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Enumerator</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>Enumerator</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4280ecb8-2449-41bd-868a-785e8ac3b3d5">ReadItem</a>
</td>
<td align="left" width="63%">
Retrieves an item from the resource and  returns an XML representation of the item.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Enumerator</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5e80674a-7889-4753-b0dd-4d7b44eba00a">AtEndOfStream</a>


</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether there are more items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/08a6307b-3ed5-4d7f-aa22-a666d64371b5">Error</a>


</td>
<td align="left" width="63%">
Gets an XML representation of additional error information.

</td>
</tr>
</table> 


## -remarks



To start an enumeration, use <a href="https://msdn.microsoft.com/ed8ad3ad-d033-45cb-b681-995c5f73b12e">Session.Enumerate</a>. To do a <a href="https://msdn.microsoft.com/en-us/library/Aa384465(v=VS.85).aspx">WS-Enumeration:</a><a href="https://msdn.microsoft.com/en-us/library/Aa384465(v=VS.85).aspx">Pull</a> operation that continues reading items in the enumeration, use <a href="https://msdn.microsoft.com/4280ecb8-2449-41bd-868a-785e8ac3b3d5">Enumerator.ReadItem</a>.

The <b>Enumerator</b> object corresponds to the  <a href="https://msdn.microsoft.com/c7afac5d-946f-49ec-a7d0-de558ed2144b">IWSManEnumerator</a> interface.


#### Examples

The following VBScript code example enumerates all the disks on a remote computer specified by the fully qualified domain name (servername.domain.com). The DisplayOutput subroutine formats the data output in the same way as the WinRM.cmd tool.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Option Explicit

Const RemoteComputer = "MIG50-64D.mig.net"

Dim objWsman, objSession, strResource
Dim objResultSet

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "http://" _
    &amp; RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" _
     &amp; "wmi/root/cimv2/Win32_OperatingSystem"
Dim iFlag
iFlag = objWsman.EnumerationFlagReturnObjectAndEPR or _
    objWsman.EnumerationFlagHierarchyDeep
Set objResultSet = _
    objSession.Enumerate( strResource, "", "",  iFlag)
While Not objResultSet.AtEndOfStream
    DisplayOutput( objResultSet.ReadItem ) 
Wend


'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c50c37bf-e19a-473b-8d27-ab3bb4ec86a0">Enumerating or Listing All of the Instances of a Resource</a>



<a href="https://msdn.microsoft.com/fda2042a-8fca-4cd8-bb55-fd1c3591921e">Scripting in Windows Remote Management</a>



<a href="https://msdn.microsoft.com/bd642669-554f-40ab-bd40-235013afa077">WinRM Scripting API</a>
 

 

