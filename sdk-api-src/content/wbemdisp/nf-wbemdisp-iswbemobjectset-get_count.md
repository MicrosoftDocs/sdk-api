---
UID: NF:wbemdisp.ISWbemObjectSet.get_Count
title: ISWbemObjectSet::get_Count
author: windows-sdk-content
description: Use the Count property of the SWbemObjectSet object to determine how many items are in an SWbemObjectSet collection. This property is read-only.
old-location: wmi\swbemobjectset_count.htm
old-project: WmiSdk
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Count property [Windows Management Instrumentation], Count property [Windows Management Instrumentation],ISWbemObjectSet interface, Count property [Windows Management Instrumentation],SWbemObjectSet object, ISWbemObjectSet interface [Windows Management Instrumentation],Count property, ISWbemObjectSet.get_Count, ISWbemObjectSet::get_Count, SWbemObjectSet object [Windows Management Instrumentation],Count property, SWbemObjectSet.Count, _hmm_swbemobjectset.count, get_Count, wmi.swbemobjectset_count
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - SWbemObjectSet.Count
 - ISWbemObjectSet.Count
 - ISWbemObjectSet.get_Count
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObjectSet::get_Count


## -description


Use the 
<b>Count</b> property of the 
<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> object to determine how many items are in an 
<b>SWbemObjectSet</b> collection. This property is read-only.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read-only.


## -parameters


## -remarks



One thing to be careful of when using Count is that WMI does not keep a running tally of the number of items in a collection. If you request Count for a collection, WMI cannot instantly respond with a number; instead, it must literally count the items, enumerating the entire collection. For a collection that has relatively few items, such as services, this enumeration likely takes less than a second. Counting the number of events in an event log collection, however, can take considerably longer.

And then suppose you want to display the property values for every event in the collection. If so, WMI will have to enumerate the entire collection a second time.

<div class="alert"><b>Note</b>  If you attempt to get this property from an 
<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> object that is returned from a method where the specified flags are included the wbemFlagForwardOnly flag, you will get an wbemErrFailed error.</div>
<div> </div>



#### Examples

For the most part, the only thing you will ever do with an SWbemObjectSet is enumerate all the objects contained within the collection itself. However, the Count Count that can be useful in system administration scripting. As the name implies, Count tells you the number of items in the collection. For example, this script retrieves a collection of all the services installed on a computer and then echoes the total number of services found:

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" &amp; strComputer &amp; "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " &amp; colSWbemObjectSet.Count

</pre>
</td>
</tr>
</table></span></div>
What makes Count useful is that it can tell you whether a specific instance is available on a computer. For example, this script retrieves a collection of all the services on a computer that have the Name W3SVC. If the Count is 0 (and it is valid for collections to have no instances), that means the W3SVC service is not installed on the computer.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" &amp; strComputer &amp; "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
    ("SELECT * FROM Win32_Service WHERE Name='w3svc'")
If colSWbemObjectSet.Count = 0 Then
    Wscript.Echo "W3SVC service is not installed on target computer."
Else
    For Each objSWbemObject In colSWbemObjectSet
        ' Perform task on World Wide Web Publishing service.
    Next
End If</pre>
</td>
</tr>
</table></span></div>


