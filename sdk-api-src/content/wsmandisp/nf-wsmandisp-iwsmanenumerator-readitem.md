---
UID: NF:wsmandisp.IWSManEnumerator.ReadItem
title: IWSManEnumerator::ReadItem
author: windows-sdk-content
description: Retrieves an item from the resource and returns an XML representation of the item.
old-location: winrm\enumerator_readitem.htm
old-project: WinRM
ms.assetid: 4280ecb8-2449-41bd-868a-785e8ac3b3d5
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: Enumerator object [Windows Remote Management],ReadItem method, Enumerator.ReadItem, IWSManEnumerator.ReadItem, IWSManEnumerator::ReadItem, ReadItem, ReadItem method [Windows Remote Management], ReadItem method [Windows Remote Management],Enumerator object, winrm.enumerator_readitem, wsman.enumerator_readitem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - Enumerator.ReadItem
 - IWSManEnumerator.ReadItem
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManEnumerator::ReadItem


## -description


Retrieves an item from the  resource and  returns an XML representation of the item.


## -parameters




### -param resource

The URI of the item.


## -returns



The XML representation of the item.




## -remarks



To limit the number of items that are read, set the <a href="https://msdn.microsoft.com/1675ba12-a0c7-4e59-a013-2109780e8afe">Session.BatchItems</a> property.

Note that the freeing of the enumeration object cleans up any pending enumeration requests.

The <a href="https://msdn.microsoft.com/ed8ad3ad-d033-45cb-b681-995c5f73b12e">Session.Enumerate</a> method does not obtain a collection in the same way that a <a href="https://msdn.microsoft.com/0cceda42-fba0-4a08-90dd-43f022d0be41">WMI query</a>, such as <code>SELECT * from Win32_LogicalDisk</code>,  returns a collection in an <a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a>. To read a file as a text stream, you create  the scripting <a href="https://msdn.microsoft.com/en-us/library/312a5kbt(v=vs.84).aspx">TextStream</a> object and call the <a href="https://msdn.microsoft.com/en-us/library/h7se9d4f(v=vs.84).aspx">TextStream.Readline</a> method to read each line of the file. In a similar way, you call the <b>Session.Enumerate</b> method to obtain an <a href="https://msdn.microsoft.com/8d8b461d-06a7-4600-8b68-2faf741a394b">Enumerator</a> object and then call the <b>Enumerator.ReadItem</b> method. As in reading from the text file, you can check the <a href="https://msdn.microsoft.com/5e80674a-7889-4753-b0dd-4d7b44eba00a">Enumerator.AtEndOfStream</a> property to check for whether you have reached the end of the data items.


#### Examples

The following VBScript example calls the <a href="https://msdn.microsoft.com/ed8ad3ad-d033-45cb-b681-995c5f73b12e">Session.Enumerate</a> method to obtain a list of scheduled jobs.  The DisplayOutput subroutine uses the Winrm command line tool XML transform file (WsmTxt.xsl) to output the data in a tabular form.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "http://" &amp; RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &amp;_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set objResultSet = objSession.Enumerate( strResource )
NumOfJobs = 0

While Not objResultSet.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( objResultSet.ReadItem ) 
Wend

Wscript.Echo "There are " &amp; NumOfJobs &amp; " jobs scheduled."

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




<a href="https://msdn.microsoft.com/c50c37bf-e19a-473b-8d27-ab3bb4ec86a0">Enumerating or Listing All the Instances of a Resource</a>



<a href="https://msdn.microsoft.com/8d8b461d-06a7-4600-8b68-2faf741a394b">Enumerator</a>
 

 

