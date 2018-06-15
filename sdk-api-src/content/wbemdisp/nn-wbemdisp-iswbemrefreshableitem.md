---
UID: NN:wbemdisp.ISWbemRefreshableItem
title: ISWbemRefreshableItem
author: windows-sdk-content
description: Represents a single item in an SWbemRefresher object.
old-location: wmi\swbemrefreshableitem.htm
old-project: WmiSdk
ms.assetid: 6a12c8eb-3ef9-4292-810c-6954294fc8c7
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemRefreshableItem, SWbemRefreshableItem, SWbemRefreshableItem object [Windows Management Instrumentation], SWbemRefreshableItem object [Windows Management Instrumentation],described, _hmm_swbemrefreshableitem, wbemdisp/SWbemRefreshableItem, wmi.swbemrefreshableitem
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
 - SWbemRefreshableItem
 - ISWbemRefreshableItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemRefreshableItem interface


## -description


The 
<b>SWbemRefreshableItem</b> object represents a single item in an 
<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a> object. An 
<b>SWbemRefreshableItem</b> object is obtained through the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a> and 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406603">AddEnum</a> methods of 
<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a>. This object cannot be created by the VBScript <a href="https://msdn.microsoft.com/3acbce31-6d56-4a7a-af03-fa37b2b868be">CreateObject</a> call.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemRefreshableItem</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>SWbemRefreshableItem</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes the 
<b>SWbemRefreshableItem</b> object from the parent <a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemRefreshableItem</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f076eb01-1e71-487d-a1af-687a052b4d67">Index</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Index of the item in its parent 
<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4be5d27c-9020-4150-84ce-f9efc55be947">IsSet</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether the <b>SWbemRefreshableItem</b> object represents a single object or an object set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/91a693c0-cde4-4cf6-b85a-662cfd0333e9">Object</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Represents a single 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object that is refreshed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f52101b1-bb6e-4798-b20f-d6efd31cf7c1">ObjectSet</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Represents the object set to be refreshed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/238722e0-63e6-4907-993e-67693746d487">Refresher</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Represents the parent 
<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a> object which contains the 
<b>SWbemRefreshableItem</b> object.

</td>
</tr>
</table> 


## -remarks



The VBScript method 
<a href="https://msdn.microsoft.com/library/windows/desktop/a953c6b8-88b3-45c4-93ca-6813c5385675">GetObject</a> cannot be used to create 
<b>SWbemRefreshableItem</b> objects directly.


#### Examples

The following script illustrates the creation of an 
<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a> object and the addition of single object and enumerator 
<b>SWbemRefreshableItem</b> to it.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>' Get some namespace connections
set cimv2 = GetObject("winmgmts:root\cimv2")
set default = GetObject("winmgmts:root\default")    

' Create a refresher
set refresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object to the refresher.
' The @ is used because this is a singleton 
' system class so only one instance exists.
set item1 = refresher.Add (default, "__CIMOMIdentification=@").Object
MsgBox "WMI Version " item1
' Add an enumerator to the refresher.
' Note that the SWbemRefreshableItem.ObjectSet 
' property must be used to designate
' this as an object set rather than a single object.
set item2 = refresher.AddEnum (cimv2, "Win32_Process").ObjectSet

' Loop three times, refreshing the items

For I= 1 To 3
MsgBox "Refresh number " &amp; I
refresher.Refresh

' Iterate through the collection of
' processes in item2 with name of wscript
    For each process in item2
        If process.name = "wscript.exe" then
        MsgBox "Process " &amp; process.Name &amp; _
           " Page Faults " &amp; process.PageFaults
        End If
    Next 
Next

' Clear out the refresher
refresher.DeleteAll 

' The following should return 0
MsgBox "Number of items in Refresher after DeleteAll " _
    &amp; refresher.Count</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>
 

 

