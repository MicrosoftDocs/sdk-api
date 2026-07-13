---
UID: NF:wabapi.IWABObject.GetMe
title: IWABObject::GetMe (wabapi.h)
description: Retrieves the entry identifier of the object that has been designated as &quot;ME.&quot;
helpviewer_keywords: ["AB_NO_DIALOG","GetMe","GetMe method [Windows Address Book]","GetMe method [Windows Address Book]","IWABObject interface","IWABObject interface [Windows Address Book]","GetMe method","IWABObject.GetMe","IWABObject::GetMe","WABOBJECT_ME_NOCREATE","_wab_IWABObject_GetMe","wab._wab_IWABObject_GetMe","wabapi/IWABObject::GetMe"]
old-location: wab\_wab_IWABObject_GetMe.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\getme.htm
ms.date: 12/05/2018
ms.keywords: AB_NO_DIALOG, GetMe, GetMe method [Windows Address Book], GetMe method [Windows Address Book],IWABObject interface, IWABObject interface [Windows Address Book],GetMe method, IWABObject.GetMe, IWABObject::GetMe, WABOBJECT_ME_NOCREATE, _wab_IWABObject_GetMe, wab._wab_IWABObject_GetMe, wabapi/IWABObject::GetMe
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
req.dll: Wab32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IWABObject::GetMe
 - wabapi/IWABObject::GetMe
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IWABObject.GetMe
---

# IWABObject::GetMe


## -description

Retrieves the entry identifier of the object that has been designated 
		as "ME."

## -parameters

### -param lpIAB

Type: <b><a href="/windows/desktop/api/wabiab/nn-wabiab-iaddrbook">IAddrBook</a>*</b>

Pointer to an <a href="/windows/desktop/api/wabiab/nn-wabiab-iaddrbook">IAddrBook</a> interface 
				that specifies the address book object.

### -param ulFlags

Type: <b>ULONG</b>

Value of type <b>ULONG</b> that specifies flags 
				affecting functionality.



#### AB_NO_DIALOG

Suppresses the ME selection dialog box.



#### WABOBJECT_ME_NOCREATE

Suppresses automatic ME creation.

### -param lpdwAction

Type: <b>DWORD*</b>

Pointer to a variable of type <b>DWORD</b> that 
				receives the flag WABOBJECT_ME_NEW on return, if a new ME entry is created. 
				 The variable is used to signal creation, as opposed to selection, of a new ME entry. The variable 
				 can be <b>NULL</b>.

### -param lpsbEID

Type: <b><a href="/previous-versions/office/developer/office-2007/cc815817(v=office.12)">SBinary</a>*</b>

Pointer to a variable of type <a href="/previous-versions/office/developer/office-2007/cc815817(v=office.12)">SBinary</a> 
				that specifies the entry identifier of the ME object on return.

### -param hwnd

Type: <b>ULONG</b>

Value of type <b>ULONG</b> that specifies 
				the handle of the parent window for displayed dialog boxes. 
				You must cast the parent <b>HWND</b> to a 
				<b>ULONG</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Users can designate a single entry in the Windows Address Book (WAB) 
that represents them. This entry is referred to as "ME." Applications desiring information about the WAB user can access 
this entry to obtain such information. The <b>IWABObject::GetMe</b> 
method returns the entry identifier of the object that has been designated as "ME." 
The application can then open this object using the entry identifier to inspect its 
properties.

If an application calls <b>IWABObject::GetMe</b> when no ME entry 
exists in the WAB, the WAB opens a dialog box that requests the user to create a new ME entry or designate 
an existing entry in the WAB as being the ME entry. 

If an application passes the <b>AB_NO_DIALOG</b> 
flag in the <i>ulFlags</i> parameter, and no ME entry already exists, the 
selection dialog box is not displayed and a new entry is automatically created.


If the user of the application calls the <b>IWABObject::GetMe</b> method to check for the existence of "ME" but does not want a new ME entry to be created automatically, the application must pass <b>WABOBJECT_ME_NOCREATE</b>. This flag prevents the creation of a new entry. If an existing ME entry is not found, the call to <b>IWABObject::GetMe</b> fails, returning MAPI_E_NOT_FOUND.

<div class="alert"><b>Note</b>  (Microsoft Internet Explorer 5 
and later) If the user or the calling application informs 
the WAB that a new ME object should be created, 
the WAB creates the new object and tries to pre-populate it 
with data that the user may have previously entered using the Registration 
Wizard in Windows 98 and Windows 2000. This pre-populated 
information will be displayed to the user so that the user has the option 
of changing it as necessary.
</div>
<div> </div>