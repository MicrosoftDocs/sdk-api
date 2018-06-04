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
 

 

