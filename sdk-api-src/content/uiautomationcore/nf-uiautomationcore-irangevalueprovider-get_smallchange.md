---
UID: NF:uiautomationcore.IRangeValueProvider.get_SmallChange
title: IRangeValueProvider::get_SmallChange
author: windows-sdk-content
description: Specifies the value that is added to or subtracted from the IRangeValueProvider::Value property when a small change is made, such as when an arrow key is pressed.
old-location: winauto\uiauto_IRangeValueProvider_SmallChange.htm
tech.root: WinAuto
ms.assetid: 8230747d-d8c3-4708-a77a-7c76a62f39dd
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IRangeValueProvider interface [Windows Accessibility],SmallChange property, IRangeValueProvider.SmallChange, IRangeValueProvider.get_SmallChange, IRangeValueProvider::SmallChange, IRangeValueProvider::get_SmallChange, SmallChange property [Windows Accessibility], SmallChange property [Windows Accessibility],IRangeValueProvider interface, get_SmallChange, uiauto.uiauto_IRangeValueProvider_SmallChange, uiauto_IRangeValueProvider_SmallChange, uiautomationcore/IRangeValueProvider::SmallChange, uiautomationcore/IRangeValueProvider::get_SmallChange, winauto.uiauto_IRangeValueProvider_SmallChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Uiautomationcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiautomationcore.dll
api_name:
 - IRangeValueProvider.SmallChange
 - IRangeValueProvider.get_SmallChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRangeValueProvider::get_SmallChange


## -description


Specifies the value that is added to or subtracted from the <a href="https://msdn.microsoft.com/b17ca8c8-948b-4d92-a6c7-79e610aa8e4a">IRangeValueProvider::Value</a> property 
        when a small change is made, such as when an arrow key is pressed.
        

This property is read-only.


## -parameters


## -remarks



The SmallChange property can support Not a Number (NaN) value. When returning a NaN value, the provider should return a quiet (non-signaling) NaN to avoid raising an exception if floating-point exceptions are turned on. The following example shows how to create a quiet NaN:

            

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



## -see-also




<a href="https://msdn.microsoft.com/1e9e39f9-e728-4ed6-bc62-80d3bbe6302d">IRangeValueProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

