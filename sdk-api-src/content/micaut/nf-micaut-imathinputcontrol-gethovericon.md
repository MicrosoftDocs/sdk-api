---
UID: NF:micaut.IMathInputControl.GetHoverIcon
title: IMathInputControl::GetHoverIcon (micaut.h)
description: Retrieves the icon to be used for the hover target to launch math input control.
helpviewer_keywords: ["GetHoverIcon","GetHoverIcon method [Tablet PC]","GetHoverIcon method [Tablet PC]","IMathInputControl interface","IMathInputControl interface [Tablet PC]","GetHoverIcon method","IMathInputControl.GetHoverIcon","IMathInputControl::GetHoverIcon","micaut/IMathInputControl::GetHoverIcon","tablet.imathinputcontrol_gethovericon"]
old-location: tablet\imathinputcontrol_gethovericon.htm
tech.root: tablet
ms.assetid: 281695e6-295b-42d8-a184-c5a005de10e3
ms.date: 12/05/2018
ms.keywords: GetHoverIcon, GetHoverIcon method [Tablet PC], GetHoverIcon method [Tablet PC],IMathInputControl interface, IMathInputControl interface [Tablet PC],GetHoverIcon method, IMathInputControl.GetHoverIcon, IMathInputControl::GetHoverIcon, micaut/IMathInputControl::GetHoverIcon, tablet.imathinputcontrol_gethovericon
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
 - IMathInputControl::GetHoverIcon
 - micaut/IMathInputControl::GetHoverIcon
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
 - IMathInputControl.GetHoverIcon
---

# IMathInputControl::GetHoverIcon


## -description

Retrieves the icon to be used for the hover target to launch math input control.

## -parameters

### -param HoverImage [out, retval]

The address of the pointer to the hover target icon.

## -returns

The method returns an <b>HRESULT</b>. Possible return codes include, but are not limited to, those in the following table.

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
The icon could not be retrieved.

</td>
</tr>
</table>

## -remarks

Applications are strongly encouraged to use this icon if implementing a hover target.
The icon is returned in .ico format and will match the system dots per inch (DPI) setting.  
      

The icon is provided as a 32-bit image with fixed width and height. 
At 96 DPI, the values are Width = 63, Height = 49. 
For other DPIs these values are changed accordingly. 
For example, on a 144 DPI system: Width = 63 * 144 / 96 and Height = 49 *144 / 96. 
The application that retrieves the hover icon is responsible for releasing the icon resources.  
      


#### Examples


```cpp

CComPtr <IMathInputControl> g_spMIC; // Math Input Control

BOOL TestDlg::OnInitDialog(){
    
    HRESULT hr = CoInitialize(NULL);
    hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);

    CComPtr<IPictureDisp> hoverImage;
    CComPtr<IPicture> pictureHoverImage;  

    g_spMIC->GetHoverIcon(&hoverImage); 

    hoverImage.QueryInterface(&pictureHoverImage);

    short type;
    pictureHoverImage->get_Type(&type);
    
    if (type == PICTYPE_ICON){
        OLE_HANDLE oleHandle;
        hr = pictureHoverImage->get_Handle(&oleHandle);        

        this->SetIcon((HICON)oleHandle, true);
    }    
    
    return TRUE;
}
```

## -see-also

<a href="/windows/desktop/api/micaut/nn-micaut-imathinputcontrol">IMathInputControl</a>