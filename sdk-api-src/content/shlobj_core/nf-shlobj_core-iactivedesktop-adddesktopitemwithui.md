---
UID: NF:shlobj_core.IActiveDesktop.AddDesktopItemWithUI
title: IActiveDesktop::AddDesktopItemWithUI (shlobj_core.h)
description: Adds a desktop item to the Active Desktop after displaying user interfaces that confirm the addition of the desktop item, verifying security zone permissions, and asking if the user wants to create a subscription.
helpviewer_keywords: ["AddDesktopItemWithUI","AddDesktopItemWithUI method [Legacy Windows Environment Features]","AddDesktopItemWithUI method [Legacy Windows Environment Features]","IActiveDesktop interface","DTI_ADDUI_DEFAULT","DTI_ADDUI_DISPSUBWIZARD","DTI_ADDUI_POSITIONITEM","IActiveDesktop interface [Legacy Windows Environment Features]","AddDesktopItemWithUI method","IActiveDesktop.AddDesktopItemWithUI","IActiveDesktop::AddDesktopItemWithUI","_win32_IActiveDesktop_AddDesktopItemWithUI_Method","lwef.iactivedesktop_adddesktopitemwithui_method","shell.iactivedesktop_adddesktopitemwithui_method","shlobj_core/IActiveDesktop::AddDesktopItemWithUI"]
old-location: lwef\iactivedesktop_adddesktopitemwithui_method.htm
tech.root: lwef
ms.assetid: ac582bd7-9fd1-4134-a866-69319ef3d96e
ms.date: 12/05/2018
ms.keywords: AddDesktopItemWithUI, AddDesktopItemWithUI method [Legacy Windows Environment Features], AddDesktopItemWithUI method [Legacy Windows Environment Features],IActiveDesktop interface, DTI_ADDUI_DEFAULT, DTI_ADDUI_DISPSUBWIZARD, DTI_ADDUI_POSITIONITEM, IActiveDesktop interface [Legacy Windows Environment Features],AddDesktopItemWithUI method, IActiveDesktop.AddDesktopItemWithUI, IActiveDesktop::AddDesktopItemWithUI, _win32_IActiveDesktop_AddDesktopItemWithUI_Method, lwef.iactivedesktop_adddesktopitemwithui_method, shell.iactivedesktop_adddesktopitemwithui_method, shlobj_core/IActiveDesktop::AddDesktopItemWithUI
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IActiveDesktop::AddDesktopItemWithUI
 - shlobj_core/IActiveDesktop::AddDesktopItemWithUI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IActiveDesktop.AddDesktopItemWithUI
---

# IActiveDesktop::AddDesktopItemWithUI


## -description

Adds a desktop item to the Active Desktop after  displaying user interfaces that confirm the addition of the desktop item, verifying security zone permissions, and asking if the user wants to create a subscription.

## -parameters

### -param hwnd [in, optional]

Type: <b>HWND</b>

The handle of the parent window. If <b>NULL</b>, the desktop item is added without displaying any user interface, in accordance with the corresponding security zone permissions. For more information, see <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537183(v=vs.85)">About URL Security Zones</a>.

### -param pcomp [in]

Type: <b>LPCOMPONENT</b>

Address of the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-component">COMPONENT</a> structure containing the details of the desktop item to be added.

### -param dwReserved

Type: <b>DWORD</b>

Unsigned long integer value that contains the flags that control how the desktop item is added. Can be one of the following values. 



#### DTI_ADDUI_DEFAULT

Do default action. Identical to using zero.



#### DTI_ADDUI_DISPSUBWIZARD

Activate the subscription wizard to allow the user to subscribe to this desktop item.



#### DTI_ADDUI_POSITIONITEM

Instruct the system to look at the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-comppos">COMPPOS</a> structure passed to the <b>cpPos</b> member of the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-component">COMPONENT</a> structure to ensure that the values are within reasonable limits. This value was added for Internet Explorer 5.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failed to add the desktop item, or an instance of the desktop item already exists on the Active Desktop.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVAILDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
If the <b>ADDURL_SILENT</b> flag has been set, the desktop item has either been added successfully or it already exists on the Active Desktop. Otherwise, the desktop item has been added successfully. 

</td>
</tr>
</table>

## -remarks

This method creates a second instance of the <a href="/windows/desktop/lwef/active-desktop-interface">Active Desktop</a> to add the desktop item, so the desktop item does not appear in the current instance. The application must call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on this <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a> interface and then use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve the Active Desktop object with the newly added component.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>



<a href="/windows/desktop/lwef/active-desktop-interface">Using the Active Desktop Object</a>