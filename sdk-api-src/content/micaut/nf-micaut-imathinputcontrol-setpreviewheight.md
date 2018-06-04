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

# IMathInputControl::SetPreviewHeight


## -description


 Modifies the preview-area height in pixels.


## -parameters




### -param Height [in]

The preview-area height in pixels.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The height specified by the <i>Height</i> parameter is outside the control's bounds.

</td>
</tr>
</table>
 




## -remarks



The preview area has predefined minimum and maximum sizes that depend on the current height of the control.
If the method returns <b>S_FALSE</b>, the <a href="https://msdn.microsoft.com/3b3404f5-b775-483f-b3a9-9467c937226b">GetPreviewHeight</a> method will return the actual size characteristics of the control.

The following image shows the Math Input Control with the default preview height.



<img alt="Math input control with default preview height" src="images/mic.png"/>
The following image shows the Math Input Control with a custom preview height.



<img alt="Math input control with custom preview height" src="images/mic_big_preview.png"/>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
    CComPtr&lt;IMathInputControl&gt; g_spMIC; // Math Input Control
        
    // Set the preview height
    // Note:  Control must be initialized first
    void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
    {
      LONG height = 200;
      HRESULT hr = S_OK;
      hr = g_spMIC-&gt;SetPreviewHeight(height);
    }          
        </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/922562be-4d5b-45b6-ad0b-49176f893c8e">Customizing the Math Input Control</a>



<a href="https://msdn.microsoft.com/3b3404f5-b775-483f-b3a9-9467c937226b">GetPreviewHeight</a>



<a href="https://msdn.microsoft.com/3d6a6289-7be5-4cf0-8cb7-9095c4ee7149">IMathInputControl</a>
 

 

