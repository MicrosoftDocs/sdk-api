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

# IDsAdminNewObjExt::AddPages


## -description


The <b>IDsAdminNewObjExt::AddPages</b> method is called to enable the object creation wizard extension to add the desired  pages to the wizard.


## -parameters




### -param lpfnAddPage [in]

Pointer to a function that the object creation wizard extension calls to add a page to the wizard. This function takes the following format.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL fnAddPage(HPROPSHEETPAGE hPage, LPARAM lParam);</pre>
</td>
</tr>
</table></span></div>
<i>hPage</i> contains the handle of the wizard page created by calling <a href="_win32_createpropertysheetpage_cpp">CreatePropertySheetPage</a>.

<i>lParam</i> is the <i>lParam</i> value passed to <b>AddPages</b>.


### -param lParam [in]

Contains data that is private to the administrative snap-in. This value is passed as the second parameter to <i>lpfnAddPage</i>.


## -returns



If the method is successful,
      <b>S_OK</b> is returned. If the method fails, an OLE-defined error code is returned.




## -remarks



For each page, the wizard extension adds to the wizard, the extension fills in a <a href="_win32_propsheetpage_str_cpp">PROPSHEETPAGE</a> structure, calls the <a href="_win32_createpropertysheetpage_cpp">CreatePropertySheetPage</a> function to create the page handle and then calls the <i>lpfnAddPage</i> function with the page handle and <i>lParam</i>.

This method is identical in format and operation to the <a href="_win32_ishellpropsheetext_win32_ishellpropsheetext_addpages_cpp">IShellPropSheetExt::AddPages</a> method.




## -see-also




<a href="_win32_createpropertysheetpage_cpp">CreatePropertySheetPage</a>



<a href="https://msdn.microsoft.com/a9b98647-b801-4a2a-98a4-d57679c07d55">IDsAdminNewObjExt</a>



<a href="_win32_ishellpropsheetext_win32_ishellpropsheetext_addpages_cpp">IShellPropSheetExt::AddPages</a>



<a href="_win32_propsheetpage_str_cpp">PROPSHEETPAGE</a>
 

 

