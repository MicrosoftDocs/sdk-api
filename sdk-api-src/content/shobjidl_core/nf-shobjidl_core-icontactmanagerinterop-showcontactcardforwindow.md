---
UID: NF:shobjidl_core.IContactManagerInterop.ShowContactCardForWindow
title: IContactManagerInterop::ShowContactCardForWindow (shobjidl_core.h)
description: Displays the UI for a contact on the specified window.
helpviewer_keywords: ["FP_ABOVE","FP_BELOW","FP_DEFAULT","FP_LEFT","FP_RIGHT","IContactManagerInterop interface [Windows Shell]","ShowContactCardForWindow method","IContactManagerInterop.ShowContactCardForWindow","IContactManagerInterop::ShowContactCardForWindow","ShowContactCardForWindow","ShowContactCardForWindow method [Windows Shell]","ShowContactCardForWindow method [Windows Shell]","IContactManagerInterop interface","shell.IContactManagerInterop_ShowContactCardForWindow","shobjidl_core/IContactManagerInterop::ShowContactCardForWindow"]
old-location: shell\IContactManagerInterop_ShowContactCardForWindow.htm
tech.root: shell
ms.assetid: 2B32B3DB-A423-4BDF-9ED1-9C1BB5B0533D
ms.date: 12/05/2018
ms.keywords: FP_ABOVE, FP_BELOW, FP_DEFAULT, FP_LEFT, FP_RIGHT, IContactManagerInterop interface [Windows Shell],ShowContactCardForWindow method, IContactManagerInterop.ShowContactCardForWindow, IContactManagerInterop::ShowContactCardForWindow, ShowContactCardForWindow, ShowContactCardForWindow method [Windows Shell], ShowContactCardForWindow method [Windows Shell],IContactManagerInterop interface, shell.IContactManagerInterop_ShowContactCardForWindow, shobjidl_core/IContactManagerInterop::ShowContactCardForWindow
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IContactManagerInterop::ShowContactCardForWindow
 - shobjidl_core/IContactManagerInterop::ShowContactCardForWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IContactManagerInterop.ShowContactCardForWindow
---

# IContactManagerInterop::ShowContactCardForWindow


## -description

Displays the UI for a contact on the specified window.

## -parameters

### -param appWindow [in]

Type: <b>HWND</b>

The <a href="/windows/desktop/WinProg/windows-data-types">HWND</a> of the foreground window of the app from which the contact card is launched and where focus is returned when the contact card is dismissed.

### -param contact [in]

Type: <b>IUnknown*</b>

A pointer to the contact object. Use a <a href="/uwp/api/windows.applicationmodel.contacts.contact">Windows.ApplicationModel.Contacts.Contact</a> object but cast to <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> here because classic COM IDL can't use Windows Runtime types.

### -param selection [in]

Type: <b>RECT const*</b>

The <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a> is the rectangular area of user selection (for example, pressing a button), around which the operating system displays the contact card, not within that rectangular area. For example, if an app uses a button to show the contact card, pass the <b>Rect</b> of the button so the contact card displays around the button, not overlapping it.

### -param preferredPlacement [in]

Type: <b>FLYOUT_PLACEMENT</b>

A <b>FLYOUT_PLACEMENT</b>-typed value that describes the preferred placement of the contact card.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FP_DEFAULT"></a><a id="fp_default"></a><dl>
<dt><b>FP_DEFAULT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Use the default.

</td>
</tr>
<tr>
<td width="40%"><a id="FP_ABOVE"></a><a id="fp_above"></a><dl>
<dt><b>FP_ABOVE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Prefer to place the contact card above the rectangular area of user selection specified by the <i>selection</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="FP_BELOW"></a><a id="fp_below"></a><dl>
<dt><b>FP_BELOW</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Prefer to place the contact card below the rectangular area of user selection specified by the <i>selection</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="FP_LEFT"></a><a id="fp_left"></a><dl>
<dt><b>FP_LEFT</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Prefer to place the contact card to the left of the rectangular area of user selection specified by the <i>selection</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="FP_RIGHT"></a><a id="fp_right"></a><dl>
<dt><b>FP_RIGHT</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Prefer to place the contact card to the right of the rectangular area of user selection specified by the <i>selection</i> parameter. 

</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>


<a href="/previous-versions/dn302110(v=vs.85)">ShowContactCardForWindow</a> returns:
            
          

<ul>
<li>S_OK if the contact card is successfully displayed</li>
<li>E_POINTER if <i>appWindow</i> is NULL or <i>contact</i> is NULL or <i>selection</i> is NULL</li>
<li>E_INVALIDARG if <i>contact</i> isn't a <a href="/uwp/api/windows.applicationmodel.contacts.contact">Windows.ApplicationModel.Contacts.Contact</a> object or <i>preferredPlacement</i> is an invalid enumeration value</li>
</ul>
Other <a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a> values are possible.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontactmanagerinterop">IContactManagerInterop</a>



<a href="/previous-versions/dn302110(v=vs.85)">ShowContactCardForWindow</a>