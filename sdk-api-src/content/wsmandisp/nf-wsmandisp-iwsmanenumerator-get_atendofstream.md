---
UID: NF:wsmandisp.IWSManEnumerator.get_AtEndOfStream
title: IWSManEnumerator::get_AtEndOfStream
author: windows-sdk-content
description: Gets a Boolean value that indicates whether there are any more items in the collection.
old-location: winrm\enumerator_atendofstream.htm
old-project: winrm
ms.assetid: 5e80674a-7889-4753-b0dd-4d7b44eba00a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AtEndOfStream property [Windows Remote Management], AtEndOfStream property [Windows Remote Management],Enumerator object, Enumerator object [Windows Remote Management],AtEndOfStream property, Enumerator.AtEndOfStream, False, IWSManEnumerator.get_AtEndOfStream, IWSManEnumerator::get_AtEndOfStream, True, get_AtEndOfStream, winrm.enumerator_atendofstream, wsman.enumerator_atendofstream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsmandisp.h
req.include-header: 
req.redist: 
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
 - Enumerator.AtEndOfStream
 - IWSManEnumerator.get_AtEndOfStream
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManEnumerator::get_AtEndOfStream


## -description


Gets a Boolean value that indicates whether there are any more items in the collection.

This property is read-only.


## -parameters


## -remarks



If you free the <a href="https://msdn.microsoft.com/8d8b461d-06a7-4600-8b68-2faf741a394b">Enumerator</a> object after you have obtained all the data required, then any pending enumeration requests are  removed. For more information, see <a href="https://msdn.microsoft.com/c50c37bf-e19a-473b-8d27-ab3bb4ec86a0">Enumerating or Listing All of the Instances of a Resource</a>.


#### Examples

The following VBScript example enumerates  operating system instances. Note that the freeing of the enumeration object cleans up any pending enumeration requests. The DisplayOutput subroutine formats the data output in the same way as the WinRM.cmd tool.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "http://" &amp; _
    RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &amp;_
    "wmi/root/cimv2/Win32_OperatingSystem"

Set objResultSet = objSession.Enumerate( strResource )

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



<a href="https://msdn.microsoft.com/8d8b461d-06a7-4600-8b68-2faf741a394b">Enumerator</a>
 

 

