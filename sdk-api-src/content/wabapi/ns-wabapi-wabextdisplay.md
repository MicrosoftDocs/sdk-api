---
UID: NS:wabapi._WABEXTDISPLAY
title: WABEXTDISPLAY (wabapi.h)
description: Do not use. Used by the Windows Address Book (WAB) to initialize user's IContextMenu Interface and IShellPropSheetExt Interface implementations.
helpviewer_keywords: ["*LPWABEXTDISPLAY","LPWABEXTDISPLAY","LPWABEXTDISPLAY structure pointer [Windows Address Book]","WABEXTDISPLAY","WABEXTDISPLAY structure [Windows Address Book]","WAB_CONTEXT_ADRLIST","WAB_DISPLAY_LDAPURL","_wab_WABEXTDISPLAY","wab._wab_WABEXTDISPLAY","wabapi/LPWABEXTDISPLAY","wabapi/WABEXTDISPLAY"]
old-location: wab\_wab_WABEXTDISPLAY.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\wabextdisplay.htm
ms.date: 12/05/2018
ms.keywords: '*LPWABEXTDISPLAY, LPWABEXTDISPLAY, LPWABEXTDISPLAY structure pointer [Windows Address Book], WABEXTDISPLAY, WABEXTDISPLAY structure [Windows Address Book], WAB_CONTEXT_ADRLIST, WAB_DISPLAY_LDAPURL, _wab_WABEXTDISPLAY, wab._wab_WABEXTDISPLAY, wabapi/LPWABEXTDISPLAY, wabapi/WABEXTDISPLAY'
req.header: wabapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WABEXTDISPLAY, *LPWABEXTDISPLAY
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - _WABEXTDISPLAY
 - wabapi/_WABEXTDISPLAY
 - LPWABEXTDISPLAY
 - wabapi/LPWABEXTDISPLAY
 - WABEXTDISPLAY
 - wabapi/WABEXTDISPLAY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wabapi.h
api_name:
 - WABEXTDISPLAY
---

# WABEXTDISPLAY structure


## -description

Do not use. Used by the Windows Address Book (WAB) to initialize user's <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu Interface</a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext">IShellPropSheetExt Interface</a> implementations.

## -struct-fields

### -field cbSize

Type: <b>ULONG</b>

Not used.

### -field lpWABObject

Type: <b>LPWABOBJECT</b>

Pointer to an <a href="/windows/desktop/api/wabapi/nn-wabapi-iwabobject">IWABObject</a> interface that specifies the object to use for calling the <b>IWABObject</b> memory allocation methods. These methods allocate any memory that you pass back to the WAB and that you expect the WAB to free or use. You can also use this pointer to call any of the other <b>IWABObject</b> methods.

### -field lpAdrBook

Type: <b>LPADRBOOK</b>

Pointer to an <a href="/windows/desktop/api/wabiab/nn-wabiab-iaddrbook">IAddrBook</a> interface that specifies the object to use for calling any of the standard WAB <b>IAddrBook</b> methods.

### -field lpPropObj

Type: <b>LPMAPIPROP</b>

Pointer to an <a href="/previous-versions/office/developer/office-2007/cc839725(v=office.12)">IMailUser : IMAPIProp</a> object. This interface is relevant for both <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext">IShellPropSheetExt Interface</a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu Interface</a> implementations. For IShellPropSheetExt Interface implementations, <b>lpPropObj</b> contains the actual object being displayed. It can be either an IMailUser : IMAPIProp or <a href="/previous-versions/office/developer/office-2007/cc842393(v=office.12)">IDistList : IMAPIContainer</a> object. To determine which object <b>lpPropObj</b> is, query for its PR_OBJECT_TYPE property. You can retrieve properties from this object to populate your extension property sheets.

For <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu Interface</a> implementations, <b>lpPropObj</b> contains a valid object; however, this object does not have any properties associated with it. 
You can call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on this object to ensure that the object and any other data of interest in this <b>WABEXTDISPLAY</b> structure survives as long as you need it. 
If you call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a>, you must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on <b>lpPropObj</b> when you no longer need it.

If your application uses named properties, and you want to get the named properties relevant to you from the WAB, you can call the <a href="/previous-versions/windows/desktop/wab/-wab-iabcontainer-getidsfromnames">GetIDsfromNames</a> method on this <b>lpPropObj</b> object to retrieve any such named properties. If you want to access properties that are associated with messaging users, cast this object to an <a href="/windows/desktop/api/wabdefs/nn-wabdefs-imailuser">LPMAILUSER</a> before calling GetIDsfromNames on it.

### -field fReadOnly

Type: <b>BOOL</b>

Variable of type <b>BOOL</b> that specifies the read-only property on certain kinds of objects, such as the <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Reference">VCARD_NAME</a> attribute, <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> search results, and one-off MailUser. This member is relevant only for <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext">IShellPropSheetExt Interface</a>. If this flag is set to true, one's property sheet must set all its controls to a read-only or disabled mode, typically in response to the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message. Setting  controls to a read-only state makes the user experience more consistent.

### -field fDataChanged

Type: <b>BOOL</b>

Variable of type <b>BOOL</b> that specifies the flag indicating that a change has been made to your property sheet. This member is relevant for <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext">IShellPropSheetExt Interface</a> only. Any time the user makes a change such as adding, editing or deleting data on your property sheet, you must set this flag to true to signal to the WAB that the data on your property sheet has changed. If this flag is not set, the WAB may not persist the changes the user made to your property sheet.

### -field ulFlags

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies flags that control behavior. The following flags are valid.



#### WAB_CONTEXT_ADRLIST

Set when the WAB calls <a href="/previous-versions/ms629473(v=vs.85)">Initialize</a> prior to invoking your <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu Interface</a> methods. This flag indicates that <b>lpv</b> contains a pointer to an <a href="/windows/desktop/api/wabdefs/ns-wabdefs-adrlist">ADRLIST</a> structure. The <b>ADRLIST</b> structure contains one or more entries, each corresponding to a selected item in the WAB user interface. To retrieve and use this <b>ADRLIST</b>, cast <b>lpv</b> to an <b>LPADRLIST</b>. You can also use <b>ulFlags</b> to determine that <b>WABEXTDISPLAY</b> is being used to initialize an IContextMenu Interface operation. If <b>ulFlags</b> does not contain this flag, you can safely assume that the structure is being used for a <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext">IShellPropSheetExt Interface</a> action.



#### WAB_DISPLAY_LDAPURL

Indicates that <b>lpsz</b> contains the <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> URL that is currently being displayed.
Sometimes the WAB will display a property sheet on a contact represented by a LDAP URL. While the contact to which the LDAP URL points will be wrapped into a WAB object and placed in <b>lpPropObj</b>, the property sheet may access the URL directly.

### -field lpv

Type: <b>LPVOID</b>

Pointer that specifies miscellaneous information that is passed to your application. The current flags identify the information being represented. If <b>ulFlags</b> is set to <b>WAB_CONTEXT_ADRLIST</b>, <b>lpv</b> contains a pointer to an <a href="/windows/desktop/api/wabdefs/ns-wabdefs-adrlist">ADRLIST</a>. Cast <b>lpv</b> to an <b>ADRLIST</b> to access the contents of the <b>ADRLIST</b>. The <b>lpAdrList-&gt;cEntries</b> member contains the number of selected items. The <a href="/windows/desktop/api/wabdefs/ns-wabdefs-adrentry">ADRENTRY</a> structures in <b>lpAdrList-&gt;aEntries</b> contain <a href="/windows/desktop/api/wabdefs/ns-wabdefs-spropvalue">SPropValue</a> arrays with all of the properties pertaining to each selected item.

### -field lpsz

Type: <b>LPTSTR</b>

Variable of type <b>LPTSTR</b> that specifies a string used for passing in miscellaneous information to your application. The current flags identify the information being represented. If <b>ulFlags</b> is set to <b>WAB_DISPLAY_LDAPURL</b>, the <b>lpsz</b> member contains a pointer to a <b>NULL</b> terminated string containing the LDAP URL whose properties are being displayed.