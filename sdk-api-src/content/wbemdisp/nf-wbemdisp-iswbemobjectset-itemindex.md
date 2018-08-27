---
UID: NF:wbemdisp.ISWbemObjectSet.ItemIndex
title: ISWbemObjectSet::ItemIndex
author: windows-sdk-content
description: Returns the SWbemObject associated with the specified index into the collection.
old-location: wmi\swbemobjectset_itemindex.htm
old-project: WmiSdk
ms.assetid: 75830f78-0489-4fae-bf9c-2eee8526232e
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemObjectSet interface [Windows Management Instrumentation],ItemIndex method, ISWbemObjectSet.ItemIndex, ISWbemObjectSet::ItemIndex, ItemIndex, ItemIndex method [Windows Management Instrumentation], ItemIndex method [Windows Management Instrumentation],ISWbemObjectSet interface, ItemIndex method [Windows Management Instrumentation],SWbemObjectSet object, SWbemObjectSet object [Windows Management Instrumentation],ItemIndex method, SWbemObjectSet.ItemIndex, collections [Windows Management Instrumentation],indexing, wmi.swbemobjectset_itemindex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
req.redist: 
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
 - SWbemObjectSet.ItemIndex
 - ISWbemObjectSet.ItemIndex
 - ISWbemObjectSet.ItemIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObjectSet::ItemIndex


## -description


The <b>ItemIndex</b> method returns the <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> associated with the specified index into the collection. The index indicates the position of the element within the collection. Collection numbering starts at zero.


## -parameters




### -param lIndex

Index of the item in the collection.


### -param objWbemObject






## -returns



If successful, the requested 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object returns.




## -remarks



The <b>ItemIndex</b> method allows WMI clients scripts and applications written in any language a uniform way to manipulate a collection like an array. This method can be used with <a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> collections. Queries, such as <a href="https://msdn.microsoft.com/a78e6701-6779-4a02-b811-23b2da4f4167">SWbemServices.AssociatorsOf</a>, <a href="https://msdn.microsoft.com/33425b1c-13f5-4c3d-8f8a-2922f3e95264">SWbemServices.ReferencesTo</a>,  <a href="https://msdn.microsoft.com/6465a981-f98e-4ece-a9b6-9da8ae618bc6">SWbemServices.InstancesOf</a>, or  <a href="https://msdn.microsoft.com/06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f">SWbemServices.ExecQuery</a> return <b>SWbemObjectSet</b> collections. The <b>ItemIndex</b> method does not work with collections which do not contain <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObjects</a>, such as <a href="https://msdn.microsoft.com/0ca2601f-ed40-472e-b4f2-eee750c8c8d1">SWbemMethodSet</a>, <a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a>, <a href="https://msdn.microsoft.com/073cf2d4-f7ee-45a6-8fa6-ca77a4870346">SWbemPrivilegeSet</a>, <a href="https://msdn.microsoft.com/0edad17b-facc-4885-9ce4-561ca6f57a66">SWbemPropertySet</a>, and <a href="https://msdn.microsoft.com/7ac5469c-357b-499d-a558-30bf760c5311">SWbemQualifierSet</a>.

<b>ItemIndex</b> can also be used to obtain the single instance of a singleton class.


#### Examples

The following VBScript code example queries for a collection of all the <a href="https://msdn.microsoft.com/51206aca-4784-4d18-95ca-bc0a45691f78">Win32_Process</a> instances then displays the names of the first three processes.


```vb
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colProcesses = _
    objWMIService.Execquery("Select * from Win32_Process")
Wscript.Echo  colProcesses.ItemIndex(0).Name
Wscript.Echo  colProcesses.ItemIndex(1).Name
Wscript.Echo  colProcesses.ItemIndex(2).Name
```


Only one instance of <a href="https://msdn.microsoft.com/eb6a8cff-20a0-4211-b46a-3084e9c39246">Win32_OperatingSystem</a> exists for each operating system installation.  Creating the  <a href="https://msdn.microsoft.com/en-us/library/Bb774345(v=VS.85).aspx">GetObject</a> path to obtain the single instance is awkward so scripts normally enumerate  <b>Win32_OperatingSystem</b>  even though only one instance is available. The following VBScript code example shows how to use the <b>ItemIndex</b> method to get to the one <b>Win32_OperatingSystem</b> without  using a <b>For Each</b> loop.


```vb
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery _
    ("Select * from Win32_OperatingSystem")

Wscript.Echo "Caption: " & colOperatingSystems.ItemIndex(0).Caption
```


The following VBScript code example gets  instances associated with <a href="https://msdn.microsoft.com/eb6a8cff-20a0-4211-b46a-3084e9c39246">Win32_OperatingSystem</a>, such as <a href="https://msdn.microsoft.com/dc71f80b-6fbd-4bc8-8783-3922d8050518">Win32_SystemOperatingSystem</a>.


```vb
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colOS = _
    objWMIService.Execquery("Select * from Win32_OperatingSystem")
    Wscript.Echo  colOS.ItemIndex(0).Name

set colAssociators = colOS.ItemIndex(0).Associators_
    For Each Associator in colAssociators 
        Wscript.Echo Associator.Path_.RelPath  
    Next
```


The following code example output shows instances associated with <a href="https://msdn.microsoft.com/eb6a8cff-20a0-4211-b46a-3084e9c39246">Win32_OperatingSystem</a>.

<pre class="syntax" xml:space="preserve"><code>Windows Server 2008 
    |C:\Windows|\Device\Harddisk0\Partition1
Win32_ComputerSystem.Name="Test1"
Win32_AutochkSetting.SettingID="Windows Server 2008 
    |C:\\Windows|\\Device\\Harddisk0\\Partition1"</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a>
 

 

