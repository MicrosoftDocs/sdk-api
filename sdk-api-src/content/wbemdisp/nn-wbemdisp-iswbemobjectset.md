---
UID: NN:wbemdisp.ISWbemObjectSet
title: ISWbemObjectSet
author: windows-sdk-content
description: An SWbemObjectSet object is a collection of SWbemObject objects. For more information, see Accessing a Collection. This object cannot be created by the VBScript CreateObject call.
old-location: wmi\swbemobjectset.htm
old-project: WmiSdk
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemObjectSet, SWbemObjectSet, SWbemObjectSet object [Windows Management Instrumentation], SWbemObjectSet object [Windows Management Instrumentation],described, _hmm_swbemobjectset, wbemdisp/SWbemObjectSet, wmi.swbemobjectset
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
 - SWbemObjectSet
 - ISWbemObjectSet
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObjectSet interface


## -description


An 
<b>SWbemObjectSet</b> object is a collection of 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> objects. For more information, see 
<a href="https://msdn.microsoft.com/c1ebe529-33cb-4158-923d-124d6328fc60">Accessing a Collection</a>. This object cannot be created by the VBScript <b>CreateObject</b> call.

You can get an 
<b>SWbemObjectSet</b> object by calling any of the following methods or their asynchronous equivalents:
<ul>
<li>
<a href="https://msdn.microsoft.com/79f01853-c649-4cbe-b2fa-cff38fb4b733">SWbemObject.Associators_</a>
</li>
<li>
<a href="https://msdn.microsoft.com/30402d7d-f7cb-43b5-96b5-a8a76144e32d">SWbemObject.Instances_</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ba02da47-0bb2-40e1-af50-1c42b4be2abd">SWbemObject.References_</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c17e5d4a-016f-42ae-bc11-e21a44772ce5">SWbemObject.Subclasses_</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a78e6701-6779-4a02-b811-23b2da4f4167">SWbemServices.AssociatorsOf</a>
</li>
<li>
<a href="https://msdn.microsoft.com/06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f">SWbemServices.ExecQuery</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6465a981-f98e-4ece-a9b6-9da8ae618bc6">SWbemServices.InstancesOf</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33425b1c-13f5-4c3d-8f8a-2922f3e95264">SWbemServices.ReferencesTo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/cfe08956-7215-4e2e-a279-6e86f14e5c27">SWbemServices.SubclassesOf</a>
</li>
</ul><div class="alert"><b>Note</b>  The 
<b>SWbemObjectSet</b> object does not support the optional 
<b>Add</b> and 
<b>Remove</b> collection methods.</div><div> </div><div class="alert"><b>Note</b>  Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.  For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemObjectSet</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>SWbemObjectSet</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
</td>
<td align="left" width="63%">
Retrieves an 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object from the collection. This is the default method of the object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemObjectSet</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ee2ad6d5-c0aa-4510-ba1b-4a152d56011f">Security_</a>


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



An <b>SWbemObjectSet</b> is a collection of zero or more <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> objects. Each <b>SWbemObject</b> in a <b>SWbemObjectSet</b> can represent one of two things:

<ul>
<li>An instance of a WMI-managed resource.</li>
<li>An instance of a class definition.</li>
</ul>
The most common use of this class in WMI is as the return value for an <a href="https://msdn.microsoft.com/94d5c8ee-2d61-42af-9a22-cc0df423b245">ExecQuery</a> or <a href="https://msdn.microsoft.com/6465a981-f98e-4ece-a9b6-9da8ae618bc6">InstancesOf</a> call, as described in the following code sample:


```vb
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```


For the most part, the only thing you will ever do with an <b>SWbemObjectSet</b> is enumerate all the objects contained within the collection itself. However, <b>SWbemObjectSet</b> does include a property Count that can be useful in system administration scripting. As the name implies, Count tells you the number of items in the collection. For example, this script retrieves a collection of all the services installed on a computer and then echoes the total number of services found:

For more information on how to use this class, see <a href="https://msdn.microsoft.com/fe7e3259-9a7c-4f73-af30-192bbbace1b3">Enumerating WMI</a>.


#### Examples

The following VBScript code sample illustrates how <b>SWbemObjectSet</b> collections are manipulated.


```vb
On Error Resume Next

Set Disks = GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")

WScript.Echo "There are", Disks.Count, " Disks"

Set Disk = Disks("Win32_LogicalDisk.DeviceID=""C:""")
WScript.Echo Disk.Path_.Path

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```


The following Perl code sample illustrates how <b>SWbemObjectSet</b> collections are manipulated.


```
use strict;
use Win32::OLE;

my ($disks,$disk);

eval { $disks = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf("CIM_LogicalDisk"); };
unless($@)
{
 print "\nThere are ", $disks->{Count}, " Disks \n";

 eval { $disk = $disks->Item("Win32_LogicalDisk.DeviceID=\"C:\""); };
 unless($@)
 {
  print $disk->{Path_}->{Path}, "\n";
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```





## -see-also




<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>
 

 

