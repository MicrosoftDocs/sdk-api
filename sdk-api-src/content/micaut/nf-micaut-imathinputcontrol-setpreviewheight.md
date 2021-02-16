---
UID: NF:micaut.IMathInputControl.SetPreviewHeight
title: IMathInputControl::SetPreviewHeight (micaut.h)
description: Modifies the preview-area height in pixels.
helpviewer_keywords: ["IMathInputControl interface [Tablet PC]","SetPreviewHeight method","IMathInputControl.SetPreviewHeight","IMathInputControl::SetPreviewHeight","SetPreviewHeight","SetPreviewHeight method [Tablet PC]","SetPreviewHeight method [Tablet PC]","IMathInputControl interface","micaut/IMathInputControl::SetPreviewHeight","tablet.imathinputcontrol_setpreviewheight"]
old-location: tablet\imathinputcontrol_setpreviewheight.htm
tech.root: tablet
ms.assetid: a5e011f6-cd51-4016-ba15-c47c152bfa99
ms.date: 12/05/2018
ms.keywords: IMathInputControl interface [Tablet PC],SetPreviewHeight method, IMathInputControl.SetPreviewHeight, IMathInputControl::SetPreviewHeight, SetPreviewHeight, SetPreviewHeight method [Tablet PC], SetPreviewHeight method [Tablet PC],IMathInputControl interface, micaut/IMathInputControl::SetPreviewHeight, tablet.imathinputcontrol_setpreviewheight
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMathInputControl::SetPreviewHeight
 - micaut/IMathInputControl::SetPreviewHeight
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - micaut.h
api_name:
 - IMathInputControl.SetPreviewHeight
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
If the method returns <b>S_FALSE</b>, the <a href="/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-getpreviewheight">GetPreviewHeight</a> method will return the actual size characteristics of the control.

The following image shows the Math Input Control with the default preview height.



<img alt="Math input control with default preview height" src="./images/mic.png"/>
The following image shows the Math Input Control with a custom preview height.



<img alt="Math input control with custom preview height" src="./images/mic_big_preview.png"/>

#### Examples


```cpp

    CComPtr<IMathInputControl> g_spMIC; // Math Input Control
        
    // Set the preview height
    // Note:  Control must be initialized first
    void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
    {
      LONG height = 200;
      HRESULT hr = S_OK;
      hr = g_spMIC->SetPreviewHeight(height);
    }          
        
```

## -see-also

<a href="/windows/desktop/tablet/customizing-the-math-input-control">Customizing the Math Input Control</a>



<a href="/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-getpreviewheight">GetPreviewHeight</a>



<a href="/windows/desktop/api/micaut/nn-micaut-imathinputcontrol">IMathInputControl</a>