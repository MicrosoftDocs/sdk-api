---
UID: NF:msclus.ISClusProperties.UseDefaultValue
title: ISClusProperties::UseDefaultValue
author: windows-sdk-content
description: Used in conjunction with ClusProperties.SaveChanges to return a property to its default value.
old-location: mscs\clusproperties_usedefaultvalue.htm
old-project: mscs
ms.assetid: 6ac19293-d489-41ee-b585-6997a29591af
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusProperties collection [Failover Cluster],UseDefaultValue method, ClusProperties.UseDefaultValue, ISClusProperties.UseDefaultValue, ISClusProperties::UseDefaultValue, UseDefaultValue, UseDefaultValue method [Failover Cluster], UseDefaultValue method [Failover Cluster],ClusProperties collection, _wolf_clusproperties.usedefaultvalue, mscs.clusproperties_usedefaultvalue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msclus.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsClus.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsClus.tlb
tech.root: 
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsClus.dll
api_name:
 - ClusProperties.UseDefaultValue
 - ISClusProperties.UseDefaultValue
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusProperties::UseDefaultValue


## -description


<p class="CCE_Message">[The 
    <b>UseDefaultValue</b> method is available for 
    use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent 
    versions.]

Used in conjunction with 
    <a href="https://msdn.microsoft.com/2792025f-c434-47e0-a5e8-06a992e3a8d2">ClusProperties.SaveChanges</a> to return a 
    property to its default value.


## -parameters




### -param varIndex

A <b>Variant</b> specifying a property by name or by numeric index.


## -returns



This method does not return a value.




## -remarks



<b>UseDefaultValue</b> works in conjunction 
    with <a href="https://msdn.microsoft.com/2792025f-c434-47e0-a5e8-06a992e3a8d2">ClusProperties.SaveChanges</a> 
    as follows.

<ul>
<li><b>UseDefaultValue</b> sets the value of 
      the property in the collection to empty and flags the property as "use default."</li>
<li>When the <a href="https://msdn.microsoft.com/2792025f-c434-47e0-a5e8-06a992e3a8d2">SaveChanges</a> method is 
      invoked, any property in the collection flagged as "use default" is not written to the 
      <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a>. Instead, 
      <b>SaveChanges</b> method clears the property 
      value stored in the cluster database, causing the property to revert to its the hard-coded default value.</li>
<li>If <a href="https://msdn.microsoft.com/2792025f-c434-47e0-a5e8-06a992e3a8d2">SaveChanges</a> is successful, it 
      automatically calls <a href="https://msdn.microsoft.com/900c9401-e8f4-423a-80df-598f5edb2935">ClusProperties.Refresh</a>, 
      which reads the default value from the cluster database into the collection.</li>
</ul>
The hard-coded default value of a property is defined by the 
    <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> or by a 
    <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a>. The 
    <a href="https://msdn.microsoft.com/a5607384-57c6-4f63-b53b-693f7053765b">Cluster Properties</a> reference section documents each of 
    the properties defined by the Cluster service, including their default values.

The <a href="https://msdn.microsoft.com/900c9401-e8f4-423a-80df-598f5edb2935">ClusProperties.Refresh</a> method clears the 
    "use default" flag without affecting cluster database.


#### Examples

The following example uses 
     <b>UseDefaultValue</b> to set all of an 
     object's properties to their default values.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Option Explicit

Public Function RestoreDefaults(obj)
  Dim objProp
  Dim strOut

  For Each objProp in obj.CommonProperties
    objProp.UseDefaultValue
  Next
  objProp.CommonProperties.SaveChanges

  For Each objProp in obj.PrivateProperties
    objProp.UseDefaultValue
  Next
  objProp.PrivateProperties.SaveChanges

  For Each objProp in objProp.CommonProperties
    strOut = strOut &amp; objProp.Name &amp; " = " &amp; CStr(objProp.Value) &amp; _
             vbCrLf
  Next

  For Each objProp in objProp.CommonProperties
    strOut = strOut &amp; objProp.Name &amp; " = " &amp; CStr(objProp.Value) &amp; _
              vbCrLf
  Next

  WScript.Echo strOut

  Set objProp = Nothing

End Function
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a>
 

 

