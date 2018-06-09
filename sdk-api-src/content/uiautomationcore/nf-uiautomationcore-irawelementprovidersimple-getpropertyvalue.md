---
UID: NF:uiautomationcore.IRawElementProviderSimple.GetPropertyValue
title: IRawElementProviderSimple::GetPropertyValue
author: windows-sdk-content
description: Retrieves the value of a property supported by the Microsoft UI Automation provider.
old-location: winauto\uiauto_IRawElementProviderSimple_GetPropertyValue.htm
old-project: WinAuto
ms.assetid: 029ea063-009d-4b54-978a-4183454b2d66
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetPropertyValue, GetPropertyValue method [Windows Accessibility], GetPropertyValue method [Windows Accessibility],IRawElementProviderSimple interface, IRawElementProviderSimple interface [Windows Accessibility],GetPropertyValue method, IRawElementProviderSimple.GetPropertyValue, IRawElementProviderSimple::GetPropertyValue, uiauto.uiauto_IRawElementProviderSimple_GetPropertyValue, uiauto_IRawElementProviderSimple_GetPropertyValue, uiautomationcore/IRawElementProviderSimple::GetPropertyValue, winauto.uiauto_IRawElementProviderSimple_GetPropertyValue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IRawElementProviderSimple.GetPropertyValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRawElementProviderSimple::GetPropertyValue


## -description


Retrieves the value of a property supported by the Microsoft UI Automation provider.


## -parameters




### -param propertyId [in]

Type: <b>PROPERTYID</b>

The property identifier. For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>.


### -param pRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>*</b>

Receives the property value, or <b>VT_EMPTY</b> if the property is not supported by this
				provider. This parameter is passed uninitialized. See Remarks.



## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an  <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a> error code.

If the provider does not support the <i>propertyId</i> property, the provider should set <i>pRetVal-&gt;vt</i> to <b>VT_EMPTY</b> and return <b>S_OK</b>. 




## -remarks



If a provider is explicitly hiding the property value (that is, the provider does not supply the property, and the request is not to be passed through to other providers), it should return a pointer obtained by using the             <a href="https://msdn.microsoft.com/ba789ed0-fa34-492c-90b4-acee0adb634c">UiaGetReservedNotSupportedValue</a> function. For example: 
            

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>pRetVal-&gt;vt = VT_UNKNOWN;
UiaGetReservedNotSupportedValue(&amp;pRetVal-&gt;punkVal);</pre>
</td>
</tr>
</table></span></div>
UI Automation properties of the <b>double</b> type support Not a Number (NaN) values. When returning a NaN value, the provider should return a quiet (non-signaling) NaN to avoid raising an exception if floating-point exceptions are turned on. The following example shows how to create a quiet NaN:

            

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>ULONGLONG ulNaN = 0xFFFFFFFFFFFFFFFF;
    *pRetVal = *reinterpret_cast&lt;double*&gt;(&amp;ulNaN);</pre>
</td>
</tr>
</table></span></div>
Alternatively, you can use the following function from the standard C++ libraries:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>numeric_limits&lt;double&gt;::quiet_NaN( )</pre>
</td>
</tr>
</table></span></div>

#### Examples

The following example returns various property values. The <b>UiaIds</b> structure contains
            property identifiers; to see how it is initialized, see <a href="https://msdn.microsoft.com/9906acea-5246-4f01-8d76-03b89ff2f789">UiaLookupId</a>.
			

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT STDMETHODCALLTYPE Provider::GetPropertyValue(PROPERTYID propertyId, 
        VARIANT* pRetVal)
{
    if (propertyId == UiaIds.ControlTypeProperty)
    {
        pRetVal-&gt;vt = VT_I4;
        pRetVal-&gt;lVal = UiaIds.ButtonControlType;
    }

    // The Name property normally comes from the Caption property of the 
    // control window, if it has one. The Name is overridden here for the 
    // sake of illustration. 
    else if (propertyId == UiaIds.NameProperty)
    {
        pRetVal-&gt;vt = VT_BSTR;
        pRetVal-&gt;bstrVal = SysAllocString(L"ColorButton");
    }
    else
    {
        pRetVal-&gt;vt = VT_EMPTY;
        // UI Automation will attempt to get the property from the host 
        //window provider.
    }
    return S_OK;
}
            </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>
 

 

