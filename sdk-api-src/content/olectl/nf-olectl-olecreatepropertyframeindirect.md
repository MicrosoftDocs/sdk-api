---
UID: NF:olectl.OleCreatePropertyFrameIndirect
title: OleCreatePropertyFrameIndirect function
author: windows-sdk-content
description: Creates a property frame, that is, a property sheet dialog box, based on a structure (OCPFIPARAMS) that contains the parameters, rather than specifying separate parameters as when calling OleCreatePropertyFrame.
old-location: com\olecreatepropertyframeindirect.htm
old-project: com
ms.assetid: ccd01d38-2d8e-4509-b44f-fef6ff718558
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: OleCreatePropertyFrameIndirect, OleCreatePropertyFrameIndirect function [COM], _ctrl_OleCreatePropertyFrameIndirect, com.olecreatepropertyframeindirect, olectl/OleCreatePropertyFrameIndirect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: olectl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PARAMDATA, *LPPARAMDATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - OleCreatePropertyFrameIndirect
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# OleCreatePropertyFrameIndirect function


## -description


Creates a property frame, that is, a property sheet dialog box, based on a structure (<a href="https://msdn.microsoft.com/d65d8239-495c-4eee-bd9c-8e803fd09a06">OCPFIPARAMS</a>) that contains the parameters, rather than specifying separate parameters as when calling <a href="https://msdn.microsoft.com/06f75ac2-3ee6-4209-83cf-a4e5244a18bd">OleCreatePropertyFrame</a>.


## -parameters




### -param lpParams [in]

Pointer to the caller-allocated structure containing the creation parameters for the dialog box.


## -returns



This function supports the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following: 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The dialog box was invoked and operated successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>lpParams</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Besides <b>cbStructSize</b> (the size of the structure) and <b>dispIDInitialProperty</b>, all of the members of the <a href="https://msdn.microsoft.com/d65d8239-495c-4eee-bd9c-8e803fd09a06">OCPFIPARAMS</a> structure have the same semantics as the parameters for <a href="https://msdn.microsoft.com/06f75ac2-3ee6-4209-83cf-a4e5244a18bd">OleCreatePropertyFrame</a>. When <i>dispIDInitialProperty</i> is DISPID_UNKNOWN, the behavior of the two functions is identical.

Working in conjunction with <a href="https://msdn.microsoft.com/05e46df3-b6c8-4520-af11-21e1ff90fb9f">IPerPropertyBrowsing</a> and <a href="https://msdn.microsoft.com/65cd8f97-f88c-433c-b4e7-9dace7193ec1">IPropertyPage2</a>, <i>dispIDInitialProperty</i> allows the caller to specify which single property should be highlighted when the dialog box is made visible. This feature is not available when using <a href="https://msdn.microsoft.com/06f75ac2-3ee6-4209-83cf-a4e5244a18bd">OleCreatePropertyFrame</a>. To determine the page and property to show initially, the property frame will do the following: 

<ol>
<li>Call <b>(*ppUnk)-&gt;QueryInterface(IID_IPerPropertyBrowsing, ...)</b> to get an interface pointer to the first object.</li>
<li>Call <b>IPerPropertyBrowsing::MapPropertyToPage(dispIDInitialProperty, ...)</b> to determine which page CLSID contains the property to be highlighted. All objects for which this frame is being invoked must support the set of properties displayed in the frame.</li>
<li>When the dialog box is created, the property page with the CLSID retrieved in Step 2 is activated with <b>IPropertyPage::Activate</b>.
</li>
<li>The property frame queries the active page for <a href="https://msdn.microsoft.com/65cd8f97-f88c-433c-b4e7-9dace7193ec1">IPropertyPage2</a>.</li>
<li>If successful, the frame calls <b>IPropertyPage2::EditProperty(dispIDInitialProperty)</b> to highlight the correct field in that dialog box.
</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/d65d8239-495c-4eee-bd9c-8e803fd09a06">OCPFIPARAMS</a>



<a href="https://msdn.microsoft.com/06f75ac2-3ee6-4209-83cf-a4e5244a18bd">OleCreatePropertyFrame</a>
 

 

