---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IRawElementProviderSimple::get_HostRawElementProvider


## -description


Specifies the host provider for this element.

This property is read-only.


## -parameters


## -remarks



This property is generally the Microsoft UI Automation provider for the window of a custom control.
			UI Automation uses this provider in combination with the custom provider. For example, the runtime identifier 
			of the element is usually obtained from the host provider.

A host provider must be returned in the following cases: when the element is a fragment root, 
			when the element is a simple element (such as a push button), and when the provider is a repositioning placeholder (for more information, see <a href="uiauto_ServerSideProvider.htm">Provider Repositioning</a>). 
			 In other cases, the property should be <b>NULL</b>.


#### Examples

The following example returns the host provider for the window that hosts the control served by 
            this provider.
			

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT STDMETHODCALLTYPE Provider::get_HostRawElementProvider(IRawElementProviderSimple** pRetVal)
{
    return UiaHostProviderFromHwnd(controlHWnd, pRetVal); 
}
            </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>



<a href="https://msdn.microsoft.com/8cc8a8d8-a4e0-477e-bf3b-2fd5df2b9db1">UiaHostProviderFromHwnd</a>
 

 

