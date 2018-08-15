---
UID: NF:wbemdisp.ISWbemServices.ExecQuery
title: ISWbemServices::ExecQuery
author: windows-sdk-content
description: Executes a query to retrieve objects.
old-location: wmi\swbemservices_execquery.htm
old-project: WmiSdk
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ExecQuery, ExecQuery method [Windows Management Instrumentation], ExecQuery method [Windows Management Instrumentation],ISWbemServices interface, ExecQuery method [Windows Management Instrumentation],SWbemServices object, ISWbemServices interface [Windows Management Instrumentation],ExecQuery method, ISWbemServices.ExecQuery, ISWbemServices::ExecQuery, SWbemServices object [Windows Management Instrumentation],ExecQuery method, SWbemServices.ExecQuery, _hmm_swbemservices.execquery, wbemFlagBidirectional, wbemFlagForwardOnly, wbemFlagReturnImmediately, wbemFlagReturnWhenComplete, wbemFlagUseAmendedQualifiers, wbemQueryFlagPrototype, wmi.swbemservices_execquery
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
 - SWbemServices.ExecQuery
 - ISWbemServices.ExecQuery
 - ISWbemServices.ExecQuery
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServices::ExecQuery


## -description


The <b>ExecQuery</b> method of the 
    <a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object executes a query to 
    retrieve objects. These objects are available through the returned 
    <a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> collection.

This method is called in the semisynchronous mode. For more information, see 
    <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For an explanation of this syntax, see 
    <a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strQuery

Required. String that contains the text of the query. This parameter cannot be blank. For more information 
      on building WMI query strings, see <a href="https://msdn.microsoft.com/7e04ba37-c0e0-4304-b162-8b911f233f38">Querying with WQL</a> 
      and the <a href="https://msdn.microsoft.com/72a7ec04-9af3-41ae-9189-6e1d46803fa9">WQL</a> reference.


### -param strQueryLanguage [optional]

String that contains the query language to be used. If specified, this value must be "WQL".


### -param iFlags [optional]

Integer that determines the behavior of the query and determines whether this call returns immediately. The 
      default value for this parameter is <b>wbemFlagReturnImmediately</b>. This parameter can 
      accept the following values.



#### wbemFlagForwardOnly (32 (0x20))

Causes a forward-only enumerator to be returned. Forward-only enumerators are generally much faster and 
        use less memory than conventional enumerators, but they do not allow calls to 
        <a href="https://msdn.microsoft.com/d0773c94-30b5-4217-8a9a-0bceb9e75f02">SWbemObject.Clone_</a>.



#### wbemFlagBidirectional (0 (0x0))

Causes WMI to retain pointers to objects of the enumeration until the client releases the 
        enumerator.



#### wbemFlagReturnImmediately (16 (0x10))

Causes the call to return immediately.



#### wbemFlagReturnWhenComplete (0 (0x0))

Causes this call to block until the query is complete. This flag calls the method in the synchronous 
        mode.



#### wbemQueryFlagPrototype (2 (0x2))

Used for prototyping. This flag stops the query from happening and returns an object that looks like a 
        typical result object.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes WMI to return class amendment data with the base class definition. For more information, see 
        <a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


### -param objWbemNamedValueSet [optional]

Typically, this is undefined. Otherwise, this is an 
      <a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent 
      the context information that can be used by the provider that is servicing the request. A provider that supports 
      or requires such information must document the recognized value names, data type of the value, allowed values, 
      and semantics.


### -param objWbemObjectSet






## -returns



If no error occurs, this method returns an 
       <a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> object. This is an object collection 
       that contains the result set of the query. The caller can examine the collection using the implementation of 
       collections for the programming language you are using. For more information, see 
       <a href="https://msdn.microsoft.com/c1ebe529-33cb-4158-923d-124d6328fc60">Accessing a Collection</a>.




## -remarks



<b>ExecQuery</b> is one of the most commonly-used calls 
     to retrieve WMI information. A standard call to 
     <b>ExecQuery</b> looks like the following:

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>strComputer = "."
Set objWMIService = GetObject("winmgmts:" &amp; "{impersonationLevel=impersonate}!\\" &amp; strComputer &amp; "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return &lt;&gt; 0 Then
        Wscript.Echo "Failed " &amp;VBNewLine &amp; "Error code = " &amp; Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
</pre>
</td>
</tr>
</table></span></div>
Note that you create the <a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object with a 
    moniker that represents the appropriate namespace and security, then make the 
    <b>ExecQuery</b>  call through the service. For a more 
    complete discussion, see <a href="https://msdn.microsoft.com/90e71e17-c2e7-42ad-a72e-2b475e6163fe">Creating a WMI Script</a> and 
    <a href="https://msdn.microsoft.com/fe7e3259-9a7c-4f73-af30-192bbbace1b3">Enumerating WMI</a>.

Like the <a href="https://msdn.microsoft.com/6465a981-f98e-4ece-a9b6-9da8ae618bc6">InstancesOf</a> method, the 
     <b>ExecQuery</b> method always returns an 
     <a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> collection. Thus your WMI script must 
     enumerate the collection ExecQuery returns in order to access each managed resource instance in the collection, 
     as shown here:

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" &amp; strComputer &amp; "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " &amp; objSWbemObject.Name
Next</pre>
</td>
</tr>
</table></span></div>
Other <a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> methods that return an 
     <a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> include 
     <a href="https://msdn.microsoft.com/a78e6701-6779-4a02-b811-23b2da4f4167">AssociatorsOf</a>, 
     <a href="https://msdn.microsoft.com/33425b1c-13f5-4c3d-8f8a-2922f3e95264">ReferencesTo</a>, and 
     <a href="https://msdn.microsoft.com/cfe08956-7215-4e2e-a279-6e86f14e5c27">SubclassesOf</a>.

It is not an error for the query to return an empty result set. The 
    <b>ExecQuery</b> method returns key properties whether 
    or not the key property is requested in the <i>strQuery</i> argument. If an error occurs when 
    executing this method and you do not use the <b>wbemFlagReturnImmediately</b> flag, the 
    <a href="vsobjerr">Err</a> object 
    is not set until you attempt to access the returned object set. However, if you use the 
    <b>wbemFlagReturnWhenComplete</b> flag, the 
    Err object 
    is set when the <b>ExecQuery</b> method is called.

There are limits to the number of <b>AND</b> and <b>OR</b> keywords 
    that can be used in WQL queries.  Large numbers of WQL keywords that are used in a complex query can cause WMI to 
    return the <b>WBEM_E_QUOTA_VIOLATION</b> error code as an <b>HRESULT</b> 
    value.  The limit of WQL keywords depends on how complex the query is.


#### Examples

The following VBScript code example locates all the disk drives on the local computer and displays the 
     device ID and the type of the disk drive.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Set colDisks = GetObject( _
    "Winmgmts:").ExecQuery("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
 
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo "No root directory. Drive type could not be determined."
        Case 2
            Wscript.Echo "DeviceID= "&amp; objDisk.DeviceID &amp; "  DriveType = Removable drive" 
        Case 3
            Wscript.Echo "DeviceID= "&amp; objDisk.DeviceID &amp; "  DriveType = Local hard disk" 
        Case 4
            Wscript.Echo "DeviceID= "&amp; objDisk.DeviceID &amp; "  DriveType = Network disk" 
        Case 5
            Wscript.Echo "DeviceID= "&amp; objDisk.DeviceID &amp; "  DriveType = Compact disk" 
        Case 6
            Wscript.Echo "DeviceID= "&amp; objDisk.DeviceID &amp; "  DriveType = RAM disk" 
        Case Else
            Wscript.Echo "Drive type could not be determined."
    End Select
Next</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/90e71e17-c2e7-42ad-a72e-2b475e6163fe">Creating a WMI Script</a>



<a href="https://msdn.microsoft.com/fe7e3259-9a7c-4f73-af30-192bbbace1b3">Enumerating WMI</a>



<a href="https://msdn.microsoft.com/7e04ba37-c0e0-4304-b162-8b911f233f38">Querying with WQL</a>



<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>



<a href="https://msdn.microsoft.com/3071aeb2-adab-47aa-a10c-9796766bb630">SWbemServices.Get</a>
 

 

