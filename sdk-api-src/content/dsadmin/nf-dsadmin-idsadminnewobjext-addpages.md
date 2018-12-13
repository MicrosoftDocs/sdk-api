---
UID: NF:dsadmin.IDsAdminNewObjExt.AddPages
title: IDsAdminNewObjExt::AddPages
author: windows-sdk-content
description: The IDsAdminNewObjExt::AddPages method is called to enable the object creation wizard extension to add the desired pages to the wizard.
old-location: ad\idsadminnewobjext_addpages.htm
tech.root: ad
ms.assetid: 4e16385f-b38a-4961-95ec-c81fd538ae2b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddPages, AddPages method [Active Directory], AddPages method [Active Directory],IDsAdminNewObjExt interface, IDsAdminNewObjExt interface [Active Directory],AddPages method, IDsAdminNewObjExt.AddPages, IDsAdminNewObjExt::AddPages, _glines_idsadminnewobjext_addpages, ad.idsadminnewobjext__addpages, ad.idsadminnewobjext_addpages, dsadmin/IDsAdminNewObjExt::AddPages
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dsadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: DSAdmin.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DSAdmin.dll
api_name:
 - IDsAdminNewObjExt.AddPages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

