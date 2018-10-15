---
UID: NF:oleacc.IAccessible.get_accHelp
title: IAccessible::get_accHelp
author: windows-sdk-content
description: The IAccessible::get_accHelp method retrieves the Help property string of an object. Not all objects support this property.
old-location: winauto\iaccessible_iaccessible__get_acchelp.htm
tech.root: WinAuto
ms.assetid: ef541ef9-ae9f-4a8c-8dd1-f221eddb55c7
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accHelp method, IAccessible.get_accHelp, IAccessible::get_accHelp, _msaa_IAccessible_get_accHelp, get_accHelp, get_accHelp method [Windows Accessibility], get_accHelp method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_acchelp, oleacc/IAccessible::get_accHelp, winauto.iaccessible_iaccessible__get_acchelp
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
 - IAccessible.get_accHelp
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
---

# IAccessible::get_accHelp


## -description


The <b>IAccessible::get_accHelp</b> method retrieves the <b>Help</b> property string of an object. Not all objects support this property.


## -parameters




### -param varChild

TBD


### -param pszHelp

Type: <b>BSTR*</b>

[out, retval] Address of a <b>BSTR</b> that receives the localized string that contains the help information for the specified object, or <b>NULL</b> if no help information is available.


#### - varID [in]

Type: <b>VARIANT</b>

Specifies whether the retrieved help information belongs to the object or one of the object's child elements. This parameter is either CHILDID_SELF (to obtain information about the object) or a child ID (to obtain information about one of the object's child elements). For more information about initializing the <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a>, see <a href="https://msdn.microsoft.com/051ec5ba-540c-4ae1-b917-4c229557ca2f">How Child IDs Are Used in Parameters</a>.


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
No help information is available.

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
</table>
 




## -remarks



None of the predefined and common controls support this property.

<b>Note to server developers:  </b>Localize the string returned from this property.

This property returns a string, whereas <a href="https://msdn.microsoft.com/a8f4ae56-6bd9-4615-a87d-a4de2f7632b1">IAccessible::get_accHelpTopic</a> provides access to a Help topic in <a href="http://go.microsoft.com/fwlink/p/?linkid=177910">WinHelp</a>. Objects are not required to support both <b>IAccessible::get_accHelp</b> and <b>IAccessible::get_accHelpTopic</b>, but they must support at least one. If they easily return a string, they must support <b>IAccessible::get_accHelp</b> ; otherwise they must support <b>IAccessible::get_accHelpTopic</b>. If both are supported, <b>IAccessible::get_accHelpTopic</b> provides more detailed information.

<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example code shows one possible implementation of this method for a custom list box. Different text is displayed depending on the status of the contact in the list. For simplicity, the example does not localize the returned string.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// m_pControl is the custom control that returns this accessible object. 
// 'online' is an enumerated value. 

HRESULT STDMETHODCALLTYPE AccServer::get_accHelp( 
    VARIANT varChild,
    BSTR *pszHelp)
{
    *pszHelp = NULL;
    if (varChild.vt != VT_I4)
    {
        return E_INVALIDARG;
    }
    if (varChild.lVal == CHILDID_SELF)
    {
        *pszHelp = SysAllocString(L"Contact list.");
    }
    else
    {
        int index = (int)varChild.lVal - 1;
        CustomListControlItem* pItem = m_pControl-&gt;GetItemAt(index);
        if (pItem == NULL)
        {
            return E_INVALIDARG;
        }
        if (pItem-&gt;GetStatus() == online)
        {
            *pszHelp = SysAllocString(L"Online contact.");
        }
        else 
        {
            *pszHelp = SysAllocString(L"Offline contact.");
        }
    }
    return S_OK;
};
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3df0cc01-cc99-42a1-9d56-591e6e00e53d">Help Property</a>



<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>



<a href="https://msdn.microsoft.com/ca70c5bc-ac20-41fe-a9fe-f4a7209c5958">IAccessible::get_accDescription</a>



<a href="https://msdn.microsoft.com/a8f4ae56-6bd9-4615-a87d-a4de2f7632b1">IAccessible::get_accHelpTopic</a>



<a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a>
 

 

