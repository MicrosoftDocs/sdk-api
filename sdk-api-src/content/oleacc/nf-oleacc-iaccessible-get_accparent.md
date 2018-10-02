---
UID: NF:oleacc.IAccessible.get_accParent
title: IAccessible::get_accParent
author: windows-sdk-content
description: The IAccessible::get_accParent method retrieves the IDispatch of the object's parent. All objects support this property.
old-location: winauto\iaccessible_iaccessible__get_accparent.htm
tech.root: WinAuto
ms.assetid: 7c8c5208-ea77-47b2-913d-314ade0313f5
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accParent method, IAccessible.get_accParent, IAccessible::get_accParent, _msaa_IAccessible_get_accParent, get_accParent, get_accParent method [Windows Accessibility], get_accParent method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_accparent, oleacc/IAccessible::get_accParent, winauto.iaccessible_iaccessible__get_accparent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccessible.get_accParent
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
---

# IAccessible::get_accParent


## -description


The <b>IAccessible::get_accParent</b> method retrieves the <a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a> of the object's parent. All objects support this property.


## -parameters




### -param ppdispParent [out, retval]

Type: <b>IDispatch**</b>

 Receives the address of the parent object's <a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a> interface. If no parent exists or if the child cannot access its parent, the variable is set to <b>NULL</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.

If not successful, returns one of the values in the table that follows, or another standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>. Servers return these values, but clients must always check output parameters to ensure that they contain valid values. For more information, see <a href="https://msdn.microsoft.com/0def0349-178b-4be5-aa1d-6602dc015981">Checking IAccessible Return Values</a>.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No parent exists for this object.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>



<a href="https://msdn.microsoft.com/64b0c24d-778a-4f13-8c70-6be3436a98cd">IAccessible::get_accChild</a>



<a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a>



<a href="https://msdn.microsoft.com/c6bcd044-bf70-4eec-92ae-66f9bd836c33">Object Navigation Properties and Methods</a>
 

 

