---
UID: NF:micaut.IMathInputControl.GetHoverIcon
title: IMathInputControl::GetHoverIcon
author: windows-sdk-content
description: Retrieves the icon to be used for the hover target to launch math input control.
old-location: tablet\imathinputcontrol_gethovericon.htm
tech.root: tablet
ms.assetid: 281695e6-295b-42d8-a184-c5a005de10e3
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: GetHoverIcon, GetHoverIcon method [Tablet PC], GetHoverIcon method [Tablet PC],IMathInputControl interface, IMathInputControl interface [Tablet PC],GetHoverIcon method, IMathInputControl.GetHoverIcon, IMathInputControl::GetHoverIcon, micaut/IMathInputControl::GetHoverIcon, tablet.imathinputcontrol_gethovericon
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - micaut.h
api_name:
 - IMathInputControl.GetHoverIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
CComPtr &lt;IMathInputControl&gt; g_spMIC; // Math Input Control

BOOL TestDlg::OnInitDialog(){
    
    HRESULT hr = CoInitialize(NULL);
    hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);

    CComPtr&lt;IPictureDisp&gt; hoverImage;
    CComPtr&lt;IPicture&gt; pictureHoverImage;  

    g_spMIC-&gt;GetHoverIcon(&amp;hoverImage); 

    hoverImage.QueryInterface(&amp;pictureHoverImage);

    short type;
    pictureHoverImage-&gt;get_Type(&amp;type);
    
    if (type == PICTYPE_ICON){
        OLE_HANDLE oleHandle;
        hr = pictureHoverImage-&gt;get_Handle(&amp;oleHandle);        

        this-&gt;SetIcon((HICON)oleHandle, true);
    }    
    
    return TRUE;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3d6a6289-7be5-4cf0-8cb7-9095c4ee7149">IMathInputControl</a>
 

 

