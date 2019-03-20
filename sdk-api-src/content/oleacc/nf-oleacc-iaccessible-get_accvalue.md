---
UID: NF:oleacc.IAccessible.get_accValue
title: IAccessible::get_accValue (oleacc.h)
author: windows-sdk-content
description: The IAccessible::get_accValue method retrieves the value of the specified object. Not all objects have a value.
old-location: winauto\iaccessible_iaccessible__get_accvalue.htm
tech.root: WinAuto
ms.assetid: 8e29adec-13fb-4a85-87ac-9e8034dce147
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accValue method, IAccessible.get_accValue, IAccessible::get_accValue, _msaa_IAccessible_get_accValue, get_accValue, get_accValue method [Windows Accessibility], get_accValue method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_accvalue, oleacc/IAccessible::get_accValue, winauto.iaccessible_iaccessible__get_accvalue
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
 - IAccessible.get_accValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
---

# IAccessible::get_accValue


## -description


The <b>IAccessible::get_accValue</b> method retrieves the value of the specified object. Not all objects have a value.


## -parameters




### -param varChild [in]

Type: <b>VARIANT</b>

Specifies whether the retrieved value information belongs to the object or one of the object's child elements. This parameter is either CHILDID_SELF (to obtain information about the object) or a child ID (to obtain information about the object's child element). For more information about initializing the <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT structure</a>, see <a href="https://msdn.microsoft.com/051ec5ba-540c-4ae1-b917-4c229557ca2f">How Child IDs Are Used in Parameters</a>.


### -param pszValue [out, retval]

Type: <b>BSTR*</b>

 Address of the <b>BSTR</b> that receives a localized string that contains the object's current value.


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



Numeric values returned from scroll bar and trackbar accessible objects indicate percentages. They are integers between zero (0) and one hundred (100), inclusive, but might also be a limited range for example, between one (1) and sixteen (16). Also, some scroll bar and trackbar objects return strings that correspond to settings such as screen size or Internet security.

<b>Note to server developers:  </b>Localize the string returned from this property.




## -see-also




<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>



<a href="https://msdn.microsoft.com/89b99645-31f5-458a-ae61-a72bf1338195">Value Property</a>
 

 

