---
UID: NS:prsht._PROPSHEETPAGEA_V3
title: "_PROPSHEETPAGEA_V3"
author: windows-sdk-content
description: The PROPSHEETPAGE structure defines a page in a property sheet. For more information, see PROPSHEETPAGE in the User Interface documentation.
old-location: mmc\propsheetpage.htm
tech.root: mmc
ms.assetid: 28cbf3df-f345-4b4f-ac34-e32e63c9b6ec
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*LPPROPSHEETPAGEA_V3, LPCPROPSHEETPAGE, LPCPROPSHEETPAGE structure pointer [MMC], LPPROPSHEETPAGE, LPPROPSHEETPAGE structure pointer [MMC], PROPSHEETPAGE, PROPSHEETPAGE structure [MMC], PROPSHEETPAGEA, PROPSHEETPAGEA_LATEST, PROPSHEETPAGEA_V3, PROPSHEETPAGEW, PSP_DEFAULT, PSP_DLGINDIRECT, PSP_HASHELP, PSP_HIDEHEADER, PSP_RTLREADING, PSP_USECALLBACK, PSP_USEHEADERSUBTITLE, PSP_USEHEADERTITLE, PSP_USEHICON, PSP_USEICONID, PSP_USEREFPARENT, PSP_USETITLE, _PROPSHEETPAGEA_V3, _slate_propsheetpage, mmc.propsheetpage, prsht/LPCPROPSHEETPAGE, prsht/LPPROPSHEETPAGE, prsht/PROPSHEETPAGE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: prsht.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Prsht.h
api_name:
 - PROPSHEETPAGE
product: Windows
targetos: Windows
req.typenames: PROPSHEETPAGEA_V3, *LPPROPSHEETPAGEA_V3
req.redist: 
---

# _PROPSHEETPAGEA_V3 structure


## -description


The <b>PROPSHEETPAGE</b> structure defines a page in a property sheet. For more 
    information, see <a href="_win32_PROPSHEETPAGE_str_cpp">PROPSHEETPAGE</a> in the User 
    Interface documentation.


## -struct-fields




### -field pszHeaderTitle

(Applies if <b>_WIN32_IE</b> &gt;= 0x0400.) Header title of the page. This member 
      can specify either the identifier of a string resource or the pointer to a Unicode string that specifies the 
      header title. If <b>dwFlags</b> does not include the 
      <b>PSP_USEHEADERTITLE</b> value, this member is ignored.


### -field pszHeaderSubTitle

(Applies if <b>_WIN32_IE</b> &gt;= 0x0400.) Header subtitle of the page. This member 
      can specify either the identifier of a string resource or the pointer to a Unicode string that specifies the 
      header subtitle. If <b>dwFlags</b> does not include the 
      <b>PSP_USEHEADERSUBTITLE</b> value, this member is ignored.


### -field hActCtx

 




#### - dwFlags

A set of bit flags that enables optional attributes of the property sheet page, and indicates the valid 
      members of the <a href="_win32_PROPSHEETPAGE_str_cpp">PROPSHEETPAGE</a> structure. This 
      member can be any combination of the following values:



#### PSP_DEFAULT

Uses the default meaning for all structure members.



#### PSP_DLGINDIRECT

Creates the page from the dialog box template in memory pointed to by the 
        <b>pResource</b> member. The 
        <a href="https://msdn.microsoft.com/1cef9b14-498e-4dcb-94a5-5faa17e0774e">PropertySheet</a> function assumes that the template 
        is in writeable memory; a read-only template causes an exception on some versions of Microsoft Windows. If 
        this flag is not set, the page loads the dialog box template from the resource identified by the 
        <b>pszTemplate</b> member.



#### PSP_HASHELP

Enables the property sheet <b>Help</b> button when this page is active.



#### PSP_USECALLBACK

Calls the function specified by <b>pfnCallback</b> when creating or destroying the 
        property sheet page defined by this structure.



#### PSP_USEHICON

Uses <b>hIcon</b> as the small icon on the tab for the page.



#### PSP_USEICONID

Uses <b>pszIcon</b> as the name of the icon resource to load and use as the small 
        icon on the tab for the page.



#### PSP_USEREFPARENT

Maintains the reference count specified by <b>pcRefParent</b> for the lifetime of the 
        property sheet page created from this structure.



#### PSP_USETITLE

Uses <b>pszTitle</b> as the title of the property sheet dialog box instead of the 
        title stored in the dialog box template.



#### PSP_RTLREADING

When this page is active, displays the text of <b>pszTitle</b> using right-to-left 
        reading order on Hebrew or Arabic systems.



#### PSP_USEHEADERTITLE

Uses <b>pszHeaderTitle</b> as the header title for the page.



#### PSP_USEHEADERSUBTITLE

Uses <b>pszHeaderSubTitle</b> as the header subtitle for the page.



#### PSP_HIDEHEADER

Causes the wizard property sheet to hide the header area when this page is selected.


##### - dwFlags.PSP_DEFAULT

Uses the default meaning for all structure members.


##### - dwFlags.PSP_DLGINDIRECT

Creates the page from the dialog box template in memory pointed to by the 
        <b>pResource</b> member. The 
        <a href="https://msdn.microsoft.com/1cef9b14-498e-4dcb-94a5-5faa17e0774e">PropertySheet</a> function assumes that the template 
        is in writeable memory; a read-only template causes an exception on some versions of Microsoft Windows. If 
        this flag is not set, the page loads the dialog box template from the resource identified by the 
        <b>pszTemplate</b> member.


##### - dwFlags.PSP_HASHELP

Enables the property sheet <b>Help</b> button when this page is active.


##### - dwFlags.PSP_HIDEHEADER

Causes the wizard property sheet to hide the header area when this page is selected.


##### - dwFlags.PSP_RTLREADING

When this page is active, displays the text of <b>pszTitle</b> using right-to-left 
        reading order on Hebrew or Arabic systems.


##### - dwFlags.PSP_USECALLBACK

Calls the function specified by <b>pfnCallback</b> when creating or destroying the 
        property sheet page defined by this structure.


##### - dwFlags.PSP_USEHEADERSUBTITLE

Uses <b>pszHeaderSubTitle</b> as the header subtitle for the page.


##### - dwFlags.PSP_USEHEADERTITLE

Uses <b>pszHeaderTitle</b> as the header title for the page.


##### - dwFlags.PSP_USEHICON

Uses <b>hIcon</b> as the small icon on the tab for the page.


##### - dwFlags.PSP_USEICONID

Uses <b>pszIcon</b> as the name of the icon resource to load and use as the small 
        icon on the tab for the page.


##### - dwFlags.PSP_USEREFPARENT

Maintains the reference count specified by <b>pcRefParent</b> for the lifetime of the 
        property sheet page created from this structure.


##### - dwFlags.PSP_USETITLE

Uses <b>pszTitle</b> as the title of the property sheet dialog box instead of the 
        title stored in the dialog box template.


#### - dwSize

Size, in bytes, of the <a href="_win32_PROPSHEETPAGE_str_cpp">PROPSHEETPAGE</a> 
      structure. The size includes any extra application-defined data at the end of the structure.


#### - hIcon

A handle to the icon to use as the small icon in the tab for the page. If 
       <b>dwFlags</b> does not include the <b>PSP_USEHICON</b> value, this 
       member is ignored.


#### - hInstance

A handle to the instance from which to load the dialog box template, icon, or title string resource.


#### - lParam

Application-defined data.


#### - pResource

A pointer to a dialog box template in memory. The  
       <a href="https://msdn.microsoft.com/1cef9b14-498e-4dcb-94a5-5faa17e0774e">PropertySheet</a> function assumes that the template 
       is in writeable memory; a read-only template will cause an exception on some versions of Windows. If 
       <b>dwFlags</b> does not include the <b>PSP_DLGINDIRECT</b> value, this 
       member is ignored.


#### - pcRefParent

A pointer to the reference count value. If <b>dwFlags</b> does not include the 
      <b>PSP_USERREFPARENT</b> value, this member is ignored.


#### - pfnCallback

A pointer to an application-defined callback function that is called when the page is created and when it 
      is about to be destroyed. For more information about the callback function, see 
      <a href="https://msdn.microsoft.com/a1f77ead-99c7-4874-8c32-289775c86458">PropSheetPageProc</a>. If 
      <b>dwFlags</b> does not include the <b>PSP_USECALLBACK</b> value, this 
      member is ignored.


#### - pfnDlgProc

A pointer to the dialog box procedure for the page. The dialog box procedure must not call the 
      <a href="https://msdn.microsoft.com/925e8aa8-9d8d-4bec-a19e-ba24e78b2d10">EndDialog</a> function.


#### - pszIcon

Icon resource to use as the small icon in the tab for the page. This member can specify either the 
       identifier of the icon resource or the pointer to the string that specifies the name of the icon resource. If 
       <b>dwFlags</b> does not include the <b>PSP_USEICONID</b> value, this 
       member is ignored.


#### - pszTemplate

Dialog box template to use to create the page. This member can specify either the resource identifier of 
       the template or the address of a string that specifies the name of the template. If 
       <b>dwFlags</b> includes the <b>PSP_DLGINDIRECT</b> value, this member is 
       ignored.


#### - pszTitle

Title of the property sheet dialog box. This title overrides the title specified in the dialog box 
      template. This member can specify either the identifier of a string resource or the pointer to a string that 
      specifies the title. If <b>dwFlags</b> does not include the 
      <b>PSP_USETITLE</b> value, this member is ignored.


## -remarks



When the <a href="https://msdn.microsoft.com/1cef9b14-498e-4dcb-94a5-5faa17e0774e">PropertySheet</a> function creates the 
    page, the dialog box procedure for the page receives a 
    <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message. The 
    <i>lParam</i> parameter of this message points to the 
    <b>PROPSHEETPAGE</b> structure used to create the page.




## -see-also




<a href="https://msdn.microsoft.com/9beb0a0a-b3bf-46d0-b10c-0fc3ab25c18d">IExtendPropertySheet2</a>



<a href="https://msdn.microsoft.com/e2115929-692e-4e59-bcdb-f37b02c53224">IPropertySheetCallback</a>



<a href="https://msdn.microsoft.com/c63d5d5f-a334-4367-8a1e-252b4eb5b50d">IPropertySheetProvider</a>



<a href="_win32_PROPSHEETPAGE_str_cpp">PROPSHEETPAGE</a>
 

 

