---
UID: NF:micaut.IMathInputControl.SetPreviewHeight
title: IMathInputControl::SetPreviewHeight
author: windows-sdk-content
description: Modifies the preview-area height in pixels.
old-location: tablet\imathinputcontrol_setpreviewheight.htm
old-project: tablet
ms.assetid: a5e011f6-cd51-4016-ba15-c47c152bfa99
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IMathInputControl interface [Tablet PC],SetPreviewHeight method, IMathInputControl.SetPreviewHeight, IMathInputControl::SetPreviewHeight, SetPreviewHeight, SetPreviewHeight method [Tablet PC], SetPreviewHeight method [Tablet PC],IMathInputControl interface, micaut/IMathInputControl::SetPreviewHeight, tablet.imathinputcontrol_setpreviewheight
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: micaut.h
req.include-header: Micaut.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Micaut.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MICUIELEMENTSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - micaut.h
api_name:
 - IMathInputControl.SetPreviewHeight
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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



<img alt="Math input control with default preview height" src="./images/mic.png"/>
The following image shows the Math Input Control with a custom preview height.



<img alt="Math input control with custom preview height" src="./images/mic_big_preview.png"/>

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
 

 

