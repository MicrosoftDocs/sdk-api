---
UID: NN:uiautomationcore.IRawElementProviderFragment
title: IRawElementProviderFragment
author: windows-driver-content
description: Exposes methods and properties on UI elements that are part of a structure more than one level deep, such as a list box or list item. Implemented by Microsoft UI Automation provider.
old-location: winauto\uiauto_IRawElementProviderFragment.htm
old-project: WinAuto
ms.assetid: 63539ba9-7f13-48cf-9c8a-74c03d31e2ab
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: IRawElementProviderFragment, IRawElementProviderFragment interface [Windows Accessibility], IRawElementProviderFragment interface [Windows Accessibility],described, uiauto.uiauto_IRawElementProviderFragment, uiauto_IRawElementProviderFragment, uiautomationcore/IRawElementProviderFragment, winauto.uiauto_IRawElementProviderFragment
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationCore.dll
api_name:
-	IRawElementProviderFragment
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRawElementProviderFragment interface


## -description


Exposes methods and properties on UI elements that are part of a structure more than one level deep, 
		such as a list box or list item. Implemented by Microsoft UI Automation provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawElementProviderFragment</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRawElementProviderFragment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRawElementProviderFragment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e64956d-5ab3-46b6-87db-4b0770c8f89a">GetEmbeddedFragmentRoots</a>
</td>
<td align="left" width="63%">
Retrieves an array of root fragments that are embedded in the UI Automation tree rooted at the current element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1252353-235e-489e-8eb9-be80d4850ca4">GetRuntimeId</a>
</td>
<td align="left" width="63%">
Retrieves the runtime identifier of an element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e0caf58-a261-4a2b-8e48-368ea3ad8840">Navigate</a>
</td>
<td align="left" width="63%">
Retrieves the UI Automation element in a specified direction within the UI Automation tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/343959bc-42d0-4289-b507-7da78cee28f2">SetFocus</a>
</td>
<td align="left" width="63%">
Sets the focus to this element.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawElementProviderFragment</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/443df4af-06cd-4866-bdeb-b1770ccb9060">BoundingRectangle</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the bounding rectangle of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d3fceca3-78b2-4775-ae11-1c9e71dbf772">FragmentRoot</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the root node of the fragment.

</td>
</tr>
</table> 


## -remarks



The root node of the fragment must also support the <a href="https://msdn.microsoft.com/16e51962-915e-40ea-a7a1-6f5a5809ba05">IRawElementProviderFragmentRoot</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/16e51962-915e-40ea-a7a1-6f5a5809ba05">IRawElementProviderFragmentRoot</a>



<a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>



<b>Reference</b>
 

 

