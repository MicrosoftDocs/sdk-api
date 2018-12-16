---
UID: NF:iads.IADsClass.Qualifiers
title: IADsClass::Qualifiers
author: windows-sdk-content
description: Returns a collection of ADSI objects that describe additional qualifiers for this schema class.
old-location: adsi\iadsclass_qualifiers.htm
tech.root: adsi
ms.assetid: d05e4278-2dfb-4832-a97d-eb35253ae535
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IADsClass interface [ADSI],Qualifiers method, IADsClass.Qualifiers, IADsClass::Qualifiers, Qualifiers, Qualifiers method [ADSI], Qualifiers method [ADSI],IADsClass interface, _ds_iadsclass_qualifiers, adsi.iadsclass__qualifiers, adsi.iadsclass_qualifiers, iads/IADsClass::Qualifiers
ms.topic: method
req.header: iads.h
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
req.type-library: 
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsClass.Qualifiers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsClass::Qualifiers


## -description


The <b>IADsClass::Qualifiers</b> method is an optional method that returns a collection of ADSI objects that describe additional qualifiers for this schema class.


## -parameters




### -param ppQualifiers [out]

Address of an <a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a> pointer variable that receives the interface pointer to the ADSI collection object that represents additional limits for this schema class.


## -returns



This method supports the standard return values, as well as the following.

For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The qualifier objects are provider-specific. When supported, this method can be used to obtain extended schema data.

This method is not currently supported by any of Microsoft providers.


#### Examples

The following code example shows how to use this method.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim ads As IADs
Dim cls As IADsClass
On Error GoTo Cleanup

Set ads = GetObject("WinNT://myComputer, computer")
Set cls = GetObject(ads.Schema)
 
' Show the user where to find additional class data.
ListBox.additem "Additional class information can be found from:"
For Each q In cls.Qualifiers
    listBox.additem q.Name 
Next

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set ads = Nothing
    Set cls = Nothing
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/690b0c96-6319-42d8-8b0e-c43f46f91031">IADsClass</a>



<a href="https://msdn.microsoft.com/48645dda-ba1e-47fa-b483-120ba982451e">IADsProperty::Qualifiers</a>
 

 

