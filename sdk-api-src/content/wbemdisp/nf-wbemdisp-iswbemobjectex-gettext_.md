---
UID: NF:wbemdisp.ISWbemObjectEx.GetText_
title: ISWbemObjectEx::GetText_
author: windows-sdk-content
description: Returns an XML representation of an object or instance. The text file is formatted in the XML format specified as shown in WbemObjectTextFormatEnum.
old-location: wmi\swbemobjectex_gettext_.htm
old-project: WmiSdk
ms.assetid: 98961d94-8360-4ed7-b1b1-20b4fca45d45
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: GetText_, GetText_ method [Windows Management Instrumentation], GetText_ method [Windows Management Instrumentation],ISWbemObjectEx interface, GetText_ method [Windows Management Instrumentation],SWbemObjectEx object, ISWbemObjectEx interface [Windows Management Instrumentation],GetText_ method, ISWbemObjectEx.GetText_, ISWbemObjectEx::GetText_, SWbemObjectEx object [Windows Management Instrumentation],GetText_ method, SWbemObjectEx.GetText_, _hmm_swbemobjectex.gettext_, wmi.swbemobjectex_gettext_
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
 - SWbemObjectEx.GetText_
 - ISWbemObjectEx.GetText_
 - ISWbemObjectEx.GetText_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObjectEx::GetText_


## -description


The 
<b>GetText_</b> method of the <a href="https://msdn.microsoft.com/944d4cdc-ad35-4b53-b755-f10131a087fb">SWbemObjectEx</a> object returns an XML representation of an object or instance. The text file is formatted in the XML format specified as shown in 
<a href="https://msdn.microsoft.com/0c97d16c-e6fc-431c-8d49-943f716a4284">WbemObjectTextFormatEnum</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param iObjectTextFormat




### -param iFlags [in, optional]

Reserved operation flags. The default value is 0 (zero).


### -param objWbemNamedValueSet [in, optional]

An 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that sets context for the operation. The default is null. 

For more information about the name/value pairs permitted, see Remarks below.


### -param bsText






#### - iTextFormat [in]

Required. A value from <a href="https://msdn.microsoft.com/0c97d16c-e6fc-431c-8d49-943f716a4284">WbemObjectTextFormatEnum</a> that specifies the resulting XML format.


## -returns



This method has no return values.




## -remarks



When constructing your <a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a>, only the following name/value pairs are permitted.

<table>
<tr>
<th>Name</th>
<th>Value</th>
</tr>
<tr>
<td>LocalOnly</td>
<td>
<b>VT_BOOL</b>

If <b>TRUE</b>, only locally defined properties and methods are present in the resulting XML.  The default is <b>FALSE</b>.

</td>
</tr>
<tr>
<td>IncludeQualifiers</td>
<td>
<b>VT_BOOL</b>

If <b>TRUE</b>, qualifiers of classes, instances, properties, and methods are included in the resulting XML.  The default is <b>FALSE</b>.

</td>
</tr>
<tr>
<td>PathLevel</td>
<td>
<b>VT-I4</b>

Default is 0 (zero).  Possible values are:

<ul>
<li>0: A &lt;CLASS&gt; or &lt;INSTANCE&gt; element is created depending on whether the object is a class or instance.</li>
<li>1: A &lt;VALUE.NAMEDOBJECT&gt; element is generated.</li>
<li>2: A &lt;VALUE.OBJECTWITHLOCALPATH&gt; element is generated.</li>
<li>3: A &lt;VALUE.OBJECTWITHPATH&gt; element is generated.</li>
</ul>
</td>
</tr>
<tr>
<td>ExcludeSystemProperties</td>
<td>
<b>VT-BOOL</b>

If <b>TRUE</b>, system properties, like __NAMESPACE, are excluded from the output.

</td>
</tr>
<tr>
<td>IncludeClassOrigin</td>
<td>
<b>VT_BOOL</b>

If <b>TRUE</b>, the class origin attribute is set on the &lt;PROPERTY&gt; and &lt;METHOD&gt; elements.  The default is <b>FALSE</b>.

</td>
</tr>
</table>
 

For more information about creating an <a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a>, see <a href="https://msdn.microsoft.com/471b23f5-6c53-40e2-a2a9-0798044c9dfb">SWbemNamedValueSet.Add</a>.


#### Examples

The following script shows how to obtain an XML representation of the <a href="https://msdn.microsoft.com/e4a5aaf0-0432-4517-97b7-ac05ffd10b5b">Win32_Bios</a> class definition. By specifying a particular instance of <b>Win32_Bios</b>, you can obtain that object's data in XML.


```vb
' Connect to the default namespace (root\cimv2) with the default
' impersonation level ("impersonate") and obtain a Win32_Bios class
' object.
Set obj = GetObject("winmgmts:win32_bios")

' Use the value for the desired XML CIM DTD format. 
XMLDtd = 1
Text = obj.GetText_(XMLDtd)
wscript.echo Text
```




