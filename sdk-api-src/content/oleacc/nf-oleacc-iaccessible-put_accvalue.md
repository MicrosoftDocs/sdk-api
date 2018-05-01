---
UID: NF:oleacc.IAccessible.put_accValue
title: IAccessible::put_accValue method
author: windows-driver-content
description: The IAccessible::put_accValue method sets the value of the specified object. Not all objects have a value.
old-location: winauto\iaccessible_iaccessible__put_accvalue.htm
old-project: WinAuto
ms.assetid: 0b1e44f4-8d03-47a4-a8c5-5296059e0459
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: IAccessible, IAccessible interface [Windows Accessibility], put_accValue method, IAccessible::put_accValue, _msaa_IAccessible_put_accValue, msaa.iaccessible_iaccessible__put_accvalue, oleacc/IAccessible::put_accValue, put_accValue method [Windows Accessibility], put_accValue method [Windows Accessibility], IAccessible interface, put_accValue,IAccessible.put_accValue, winauto.iaccessible_iaccessible__put_accvalue
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
req.typenames: QACONTROL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Oleacc.dll
api_name:
-	IAccessible.put_accValue
product: Windows
targetos: Windows
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IAccessible::put_accValue method


## -description


The <b>IAccessible::put_accValue</b> method sets the value of the specified object. Not all objects have a value.


## -parameters




### -param varChild




### -param szValue






#### - pszValue [in]

Type: <b>BSTR</b>

A localized string that contains the object's value.


#### - varID [in]

Type: <b>VARIANT</b>

Specifies whether the value information being set belongs to the object or one of the object's child elements. This parameter is either CHILDID_SELF (to set information on the object) or a child ID (to set information about the object's child element). For more information about initializing the <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT structure</a>, see <a href="https://msdn.microsoft.com/051ec5ba-540c-4ae1-b917-4c229557ca2f">How Child IDs Are Used in Parameters</a>.


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
<dt><b>DISP_E_MEMBERNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The object does not support this property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An argument is not valid.

</td>
</tr>
</table>
 




## -remarks



The <b>IAccessible::put_accValue</b> method is supported for some UI elements (usually edit controls). For UI elements that do not support this method, control-specific methods are used instead. For more information, see <a href="https://msdn.microsoft.com/5d0a81d8-5d36-4c33-bb8c-abcb8b00166e">Supported User Interface Element Reference</a>.



