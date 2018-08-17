---
UID: NS:wabapi._WABEXTDISPLAY
title: "_WABEXTDISPLAY"
author: windows-sdk-content
description: Do not use. Used by the Windows Address Book (WAB) to initialize user's IContextMenu Interface and IShellPropSheetExt Interface implementations.
old-location: wab\_wab_WABEXTDISPLAY.htm
old-project: wab
ms.assetid: VS|wab|~\wab\reference\structures\wabextdisplay.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*LPWABEXTDISPLAY, LPWABEXTDISPLAY, LPWABEXTDISPLAY structure pointer [Windows Address Book], WABEXTDISPLAY, WABEXTDISPLAY structure [Windows Address Book], WAB_CONTEXT_ADRLIST, WAB_DISPLAY_LDAPURL, _WABEXTDISPLAY, _wab_WABEXTDISPLAY, wab._wab_WABEXTDISPLAY, wabapi/LPWABEXTDISPLAY, wabapi/WABEXTDISPLAY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wabapi.h
req.include-header: 
req.redist: 
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
req.typenames: WABEXTDISPLAY, *LPWABEXTDISPLAY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wabapi.h
api_name:
 - WABEXTDISPLAY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# _WABEXTDISPLAY structure


## -description


Do not use. Used by the Windows Address Book (WAB) to initialize user's <a href="_win32_IContextMenu">IContextMenu Interface</a> and <a href="_win32_IShellPropSheetExt">IShellPropSheetExt Interface</a> implementations.


## -struct-fields




### -field cbSize

Type: <b>ULONG</b>

Not used.


### -field lpWABObject

Type: <b>LPWABOBJECT</b>

Pointer to an <a href="https://msdn.microsoft.com/cba6a6ae-79e5-4412-9e1e-ad0ef41b1862">IWABObject</a> interface that specifies the object to use for calling the <b>IWABObject</b> memory allocation methods. These methods allocate any memory that you pass back to the WAB and that you expect the WAB to free or use. You can also use this pointer to call any of the other <b>IWABObject</b> methods.


### -field lpAdrBook

Type: <b>LPADRBOOK</b>

Pointer to an <a href="https://msdn.microsoft.com/df614598-b9ac-462a-89e7-cda0a602c6cd">IAddrBook</a> interface that specifies the object to use for calling any of the standard WAB <b>IAddrBook</b> methods.


### -field lpPropObj

Type: <b>LPMAPIPROP</b>

Pointer to an <a href="0555ca4a-63f9-4f80-8754-ff7e1a8322b9">IMailUser : IMAPIProp</a> object. This interface is relevant for both <a href="_win32_IShellPropSheetExt">IShellPropSheetExt Interface</a> and <a href="_win32_IContextMenu">IContextMenu Interface</a> implementations. For IShellPropSheetExt Interface implementations, <b>lpPropObj</b> contains the actual object being displayed. It can be either an IMailUser : IMAPIProp or <a href="ad706aaf-2497-4920-95fc-afe1b31f97d0">IDistList : IMAPIContainer</a> object. To determine which object <b>lpPropObj</b> is, query for its PR_OBJECT_TYPE property. You can retrieve properties from this object to populate your extension property sheets.

For <a href="_win32_IContextMenu">IContextMenu Interface</a> implementations, <b>lpPropObj</b> contains a valid object; however, this object does not have any properties associated with it. 
You can call the <a href="_com_iunknown_addref">AddRef</a> on this object to ensure that the object and any other data of interest in this <b>WABEXTDISPLAY</b> structure survives as long as you need it. 
If you call <a href="b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a>, you must call <a href="4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on <b>lpPropObj</b> when you no longer need it.

If your application uses named properties, and you want to get the named properties relevant to you from the WAB, you can call the <a href="a4fff5c7-d2ed-44c4-9859-f764a969809e">GetIDsfromNames</a> method on this <b>lpPropObj</b> object to retrieve any such named properties. If you want to access properties that are associated with messaging users, cast this object to an <a href="https://msdn.microsoft.com/7af094d9-b5fd-4214-9604-b7dd93639f5e">LPMAILUSER</a> before calling GetIDsfromNames on it.


### -field fReadOnly

Type: <b>BOOL</b>

Variable of type <b>BOOL</b> that specifies the read-only property on certain kinds of objects, such as the <a href="_inet_VCARD_NAME_Attribute_vcard_name_Property_scr">VCARD_NAME</a> attribute, <a href="_ds_ldap_api_start_page">LDAP</a> search results, and <a href="https://docs.microsoft.com/">one-off</a> MailUser. This member is relevant only for <a href="_win32_IShellPropSheetExt">IShellPropSheetExt Interface</a>. If this flag is set to true, one's property sheet must set all its controls to a read-only or disabled mode, typically in response to the <a href="_win32_wm_initdialog">WM_INITDIALOG</a> message. Setting  controls to a read-only state makes the user experience more consistent.


### -field fDataChanged

Type: <b>BOOL</b>

Variable of type <b>BOOL</b> that specifies the flag indicating that a change has been made to your property sheet. This member is relevant for <a href="_win32_IShellPropSheetExt">IShellPropSheetExt Interface</a> only. Any time the user makes a change such as adding, editing or deleting data on your property sheet, you must set this flag to true to signal to the WAB that the data on your property sheet has changed. If this flag is not set, the WAB may not persist the changes the user made to your property sheet.


### -field ulFlags

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies flags that control behavior. The following flags are valid.



#### WAB_CONTEXT_ADRLIST

Set when the WAB calls <a href="https://msdn.microsoft.com/7deef238-68d3-4c5b-8196-38de86bb2092">Initialize</a> prior to invoking your <a href="_win32_IContextMenu">IContextMenu Interface</a> methods. This flag indicates that <b>lpv</b> contains a pointer to an <a href="https://msdn.microsoft.com/4c9cc1a8-3379-4f01-9125-16ac6bbdd54b">ADRLIST</a> structure. The <b>ADRLIST</b> structure contains one or more entries, each corresponding to a selected item in the WAB user interface. To retrieve and use this <b>ADRLIST</b>, cast <b>lpv</b> to an <b>LPADRLIST</b>. You can also use <b>ulFlags</b> to determine that <b>WABEXTDISPLAY</b> is being used to initialize an IContextMenu Interface operation. If <b>ulFlags</b> does not contain this flag, you can safely assume that the structure is being used for a <a href="_win32_IShellPropSheetExt">IShellPropSheetExt Interface</a> action.



#### WAB_DISPLAY_LDAPURL

Indicates that <b>lpsz</b> contains the <a href="_ds_ldap_api_start_page">LDAP</a> URL that is currently being displayed.
Sometimes the WAB will display a property sheet on a contact represented by a LDAP URL. While the contact to which the LDAP URL points will be wrapped into a WAB object and placed in <b>lpPropObj</b>, the property sheet may access the URL directly.


### -field lpv

Type: <b>LPVOID</b>

Pointer that specifies miscellaneous information that is passed to your application. The current flags identify the information being represented. If <b>ulFlags</b> is set to <b>WAB_CONTEXT_ADRLIST</b>, <b>lpv</b> contains a pointer to an <a href="https://msdn.microsoft.com/4c9cc1a8-3379-4f01-9125-16ac6bbdd54b">ADRLIST</a>. Cast <b>lpv</b> to an <b>ADRLIST</b> to access the contents of the <b>ADRLIST</b>. The <b>lpAdrList-&gt;cEntries</b> member contains the number of selected items. The <a href="https://msdn.microsoft.com/3044ca5e-f802-4c7b-8521-7d8adc63dc1b">ADRENTRY</a> structures in <b>lpAdrList-&gt;aEntries</b> contain <a href="https://msdn.microsoft.com/cff1b41d-fc53-4987-8823-04cbd51e811b">SPropValue</a> arrays with all of the properties pertaining to each selected item.


### -field lpsz

Type: <b>LPTSTR</b>

Variable of type <b>LPTSTR</b> that specifies a string used for passing in miscellaneous information to your application. The current flags identify the information being represented. If <b>ulFlags</b> is set to <b>WAB_DISPLAY_LDAPURL</b>, the <b>lpsz</b> member contains a pointer to a <b>NULL</b> terminated string containing the LDAP URL whose properties are being displayed.

