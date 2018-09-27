---
UID: NF:shobjidl_core.IContactManagerInterop.ShowContactCardForWindow
title: IContactManagerInterop::ShowContactCardForWindow
author: windows-sdk-content
description: Displays the UI for a contact on the specified window.
old-location: shell\IContactManagerInterop_ShowContactCardForWindow.htm
tech.root: shell
ms.assetid: 2B32B3DB-A423-4BDF-9ED1-9C1BB5B0533D
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: FP_ABOVE, FP_BELOW, FP_DEFAULT, FP_LEFT, FP_RIGHT, IContactManagerInterop interface [Windows Shell],ShowContactCardForWindow method, IContactManagerInterop.ShowContactCardForWindow, IContactManagerInterop::ShowContactCardForWindow, ShowContactCardForWindow, ShowContactCardForWindow method [Windows Shell], ShowContactCardForWindow method [Windows Shell],IContactManagerInterop interface, shell.IContactManagerInterop_ShowContactCardForWindow, shobjidl_core/IContactManagerInterop::ShowContactCardForWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IContactManagerInterop.ShowContactCardForWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContactManagerInterop::ShowContactCardForWindow


## -description


Displays the UI for a contact on the specified window.


## -parameters




### -param appWindow [in]

Type: <b>HWND</b>

The <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a> of the foreground window of the app from which the contact card is launched and where focus is returned when the contact card is dismissed.


### -param contact [in]

Type: <b>IUnknown*</b>

A pointer to the contact object. Use a <a href="https://msdn.microsoft.com/07883e6f-9eda-48e1-8727-a5831fe8a3e0">Windows.ApplicationModel.Contacts.Contact</a> object but cast to <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> here because classic COM IDL can't use Windows Runtime types.


### -param selection [in]

Type: <b>RECT const*</b>

The <a href="https://msdn.microsoft.com/87f52802-3e26-4c64-a8c9-7323fec26336">Rect</a> is the rectangular area of user selection (for example, pressing a button), around which the operating system displays the contact card, not within that rectangular area. For example, if an app uses a button to show the contact card, pass the <b>Rect</b> of the button so the contact card displays around the button, not overlapping it.


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


<a href="https://msdn.microsoft.com/4BF4A5A4-9BF0-4BF0-BC2B-04C4C0C25C36">ShowContactCardForWindow</a> returns:
            
          

<ul>
<li>S_OK if the contact card is successfully displayed</li>
<li>E_POINTER if <i>appWindow</i> is NULL or <i>contact</i> is NULL or <i>selection</i> is NULL</li>
<li>E_INVALIDARG if <i>contact</i> isn't a <a href="https://msdn.microsoft.com/07883e6f-9eda-48e1-8727-a5831fe8a3e0">Windows.ApplicationModel.Contacts.Contact</a> object or <i>preferredPlacement</i> is an invalid enumeration value</li>
</ul>
Other <a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a> values are possible.




## -see-also




<a href="https://msdn.microsoft.com/8E854BA3-C29E-4911-9D6E-915D1959244C">IContactManagerInterop</a>



<a href="https://msdn.microsoft.com/4BF4A5A4-9BF0-4BF0-BC2B-04C4C0C25C36">ShowContactCardForWindow</a>
 

 

