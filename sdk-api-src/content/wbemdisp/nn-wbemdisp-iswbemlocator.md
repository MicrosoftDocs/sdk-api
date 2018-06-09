---
UID: NN:wbemdisp.ISWbemLocator
title: ISWbemLocator
author: windows-sdk-content
description: You can use the methods of the SWbemLocator object to obtain an SWbemServices object that represents a connection to a namespace on either a local computer or a remote host computer.
old-location: wmi\swbemlocator.htm
old-project: WmiSdk
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemLocator, SWbemLocator, SWbemLocator object [Windows Management Instrumentation], SWbemLocator object [Windows Management Instrumentation],described, _hmm_swbemlocator, wbemdisp/SWbemLocator, wmi.swbemlocator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemLocator
 - ISWbemLocator
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemLocator interface


## -description


You can use the methods of the 
<b>SWbemLocator</b> object to obtain an 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object that represents a connection to a namespace on either a local computer or a remote host computer. You can then use the methods of the 
<b>SWbemServices</b> object to access WMI. This object can be created by the VBScript <b>CreateObject</b> call.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemLocator</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>SWbemLocator</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31364c68-b031-4cf0-851f-b4e302f077e0">ConnectServer</a>
</td>
<td align="left" width="63%">
Connects to WMI on the specified computer.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemLocator</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/75987bef-21ae-4420-b069-afab90499218">Security_</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Used to read or change the security settings.

</td>
</tr>
</table> 


## -remarks



At the top of the WMI scripting library object model is the SWbemLocator object. SWbemLocator is used to establish an authenticated connection to a WMI namespace, much as the VBScript GetObject function and the WMI moniker "winmgmts:" are used to establish an authenticated connection to WMI. However, SWbemLocator is designed to address two specific scripting scenarios that cannot be performed using GetObject and the WMI moniker. You must use SWbemLocator if you need to:

<ul>
<li>Provide user and password credentials to connect to WMI on a remote computer. The WMI moniker used with the GetObject function does not include a mechanism for specifying credentials. Most WMI activities (including all of those carried out on remote computers) require administrator rights. If you typically log on using a regular user account instead of an administrator account, you will not be able to perform most WMI tasks unless you run the script under alternate credentials.</li>
<li>Connect to WMI if you are running a WMI script from within a Web page. You cannot use the GetObject function when running scripts embedded within an HTML page because Internet Explorer disallows the use of GetObject for security reasons.</li>
</ul>
In addition, you might want to use SWbemLocator to connect to WMI if you find the WMI connection string used with GetObject confusing or difficult.

You use CreateObject rather than GetObject to create a reference to SWbemLocator. To create the reference, you must pass the CreateObject function the SWbemLocator programmatic identifier (ProgID) "WbemScripting.SWbemLocator", as shown on line 2 in the following script sample. After you obtain a reference to an SWbemLocator object, you call the ConnectServer method to connect to WMI and obtain a reference to an SWbemServices object. This is demonstrated on line 3 of the following script.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " &amp; objSWbemObject.Name
Next</pre>
</td>
</tr>
</table></span></div>
To run a script under alternate credentials, include the user name and password as additional parameters passed to ConnectServer. For example, this script runs under the credentials of a user named kenmyer, with the password homerj.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>strComputer = "atl-dc-01"
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer _
    (strComputer, "root\cimv2", "kenmyer", "homerj")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " &amp; objSWbemObject.Name
Next</pre>
</td>
</tr>
</table></span></div>
You can also use the Domain\User Name format to specify a user name. For example:

<code>" fabrikam\kenmyer"</code>




#### Examples

The following PowerShell example uses <b>SWbemLocator</b> to connect to a server.

<div class="code"><span codelanguage="PowerShell"><table>
<tr>
<th>PowerShell</th>
</tr>
<tr>
<td>
<pre>$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>
 

 

