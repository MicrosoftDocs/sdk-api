---
UID: NF:shobjidl_core.IShellBrowser.BrowseObject
title: IShellBrowser::BrowseObject (shobjidl_core.h)
description: Informs Windows Explorer to browse to another folder.
helpviewer_keywords: ["BrowseObject","BrowseObject method [Windows Shell]","BrowseObject method [Windows Shell]","IShellBrowser interface","IShellBrowser interface [Windows Shell]","BrowseObject method","IShellBrowser.BrowseObject","IShellBrowser::BrowseObject","SBSP_ABSOLUTE","SBSP_ACTIVATE_NOFOCUS","SBSP_ALLOW_AUTONAVIGATE","SBSP_CALLERUNTRUSTED","SBSP_CREATENOHISTORY","SBSP_DEFBROWSER","SBSP_DEFMODE","SBSP_EXPLOREMODE","SBSP_FEEDNAVIGATION","SBSP_HELPMODE","SBSP_INITIATEDBYHLINKFRAME","SBSP_KEEPSAMETEMPLATE","SBSP_KEEPWORDWHEELTEXT","SBSP_NAVIGATEBACK","SBSP_NAVIGATEFORWARD","SBSP_NEWBROWSER","SBSP_NOAUTOSELECT","SBSP_NOTRANSFERHIST","SBSP_OPENMODE","SBSP_PARENT","SBSP_PLAYNOSOUND","SBSP_REDIRECT","SBSP_RELATIVE","SBSP_SAMEBROWSER","SBSP_TRUSTEDFORACTIVEX","SBSP_TRUSTFIRSTDOWNLOAD","SBSP_UNTRUSTEDFORDOWNLOAD","SBSP_WRITENOHISTORY","_win32_IShellBrowser_BrowseObject","shell.IShellBrowser_BrowseObject","shobjidl_core/IShellBrowser::BrowseObject"]
old-location: shell\IShellBrowser_BrowseObject.htm
tech.root: shell
ms.assetid: e391ca11-25e3-4d97-8efd-0afd74a3e5c2
ms.date: 12/05/2018
ms.keywords: BrowseObject, BrowseObject method [Windows Shell], BrowseObject method [Windows Shell],IShellBrowser interface, IShellBrowser interface [Windows Shell],BrowseObject method, IShellBrowser.BrowseObject, IShellBrowser::BrowseObject, SBSP_ABSOLUTE, SBSP_ACTIVATE_NOFOCUS, SBSP_ALLOW_AUTONAVIGATE, SBSP_CALLERUNTRUSTED, SBSP_CREATENOHISTORY, SBSP_DEFBROWSER, SBSP_DEFMODE, SBSP_EXPLOREMODE, SBSP_FEEDNAVIGATION, SBSP_HELPMODE, SBSP_INITIATEDBYHLINKFRAME, SBSP_KEEPSAMETEMPLATE, SBSP_KEEPWORDWHEELTEXT, SBSP_NAVIGATEBACK, SBSP_NAVIGATEFORWARD, SBSP_NEWBROWSER, SBSP_NOAUTOSELECT, SBSP_NOTRANSFERHIST, SBSP_OPENMODE, SBSP_PARENT, SBSP_PLAYNOSOUND, SBSP_REDIRECT, SBSP_RELATIVE, SBSP_SAMEBROWSER, SBSP_TRUSTEDFORACTIVEX, SBSP_TRUSTFIRSTDOWNLOAD, SBSP_UNTRUSTEDFORDOWNLOAD, SBSP_WRITENOHISTORY, _win32_IShellBrowser_BrowseObject, shell.IShellBrowser_BrowseObject, shobjidl_core/IShellBrowser::BrowseObject
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellBrowser::BrowseObject
 - shobjidl_core/IShellBrowser::BrowseObject
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
 - IShellBrowser.BrowseObject
---

# IShellBrowser::BrowseObject


## -description

Informs Windows Explorer to browse to another folder.

## -parameters

### -param pidl

Type: <b>PCUIDLIST_RELATIVE</b>

The address of an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> (item identifier list) structure that specifies an object's location. This value is dependent on the flag or flags set in the <i>wFlags</i> parameter.

### -param wFlags

Type: <b>UINT</b>

Flags specifying the folder to be browsed. It can be zero or one or more of the following values.




These flags specify whether another window is to be created.







#### SBSP_DEFBROWSER (0x0000)

Use default behavior, which respects the view option (the user setting to create new windows or to browse in place). In most cases, calling applications should use this flag.



#### SBSP_SAMEBROWSER

Browse to another folder with the same Windows Explorer window.



#### SBSP_NEWBROWSER

Creates another window for the specified folder.




The following flags specify the mode. These values are ignored if SBSP_SAMEBROWSER is specified or if SBSP_DEFBROWSER is specified and the user has selected <b>Browse In Place</b>.







#### SBSP_DEFMODE

Use the current window.



#### SBSP_OPENMODE

Specifies no folder tree for the new browse window. If the current browser does not match the SBSP_OPENMODE of the browse object call,  a new window is opened.



#### SBSP_EXPLOREMODE

Specifies a folder tree for the new browse window. If the current browser does not match the SBSP_EXPLOREMODE of the browse object call, a new window is opened.



#### SBSP_HELPMODE

Not supported. Do not use.



#### SBSP_NOTRANSFERHIST

Do not transfer the browsing history to the new window.




The following flags specify the category of the <i>pidl</i> parameter.







#### SBSP_ABSOLUTE

An absolute PIDL, relative to the desktop.



#### SBSP_RELATIVE

A relative PIDL, relative to the current folder.



#### SBSP_PARENT

Browse the parent folder, ignore the PIDL.



#### SBSP_NAVIGATEBACK

Navigate back, ignore the PIDL.



#### SBSP_NAVIGATEFORWARD

Navigate forward, ignore the PIDL.







#### SBSP_ALLOW_AUTONAVIGATE (0x00010000)

Enable auto-navigation.




The following flags specify mode.







#### SBSP_KEEPSAMETEMPLATE (0x00020000)

<b>Windows Vista and later</b>. Not supported. Do not use.



#### SBSP_KEEPWORDWHEELTEXT (0x00040000)

<b>Windows Vista and later</b>. Navigate without clearing the search entry field.



#### SBSP_ACTIVATE_NOFOCUS (0x00080000)

<b>Windows Vista and later</b>. Navigate without the default behavior of setting focus into the new view.




The following flags control how history is manipulated as a result of navigation.







#### SBSP_CALLERUNTRUSTED (0x00800000)

<b>Microsoft Internet Explorer 6 Service Pack 2 (SP2) and later</b>. The navigation was possibly initiated by a webpage with scripting code already present on the local system.



#### SBSP_TRUSTFIRSTDOWNLOAD (0x01000000)

<b>Microsoft Internet Explorer 6 Service Pack 2 (SP2) and later</b>. The new window is the result of a user initiated action. Trust the new window if it immediately attempts to download content.



#### SBSP_UNTRUSTEDFORDOWNLOAD (0x02000000)

<b>Microsoft Internet Explorer 6 Service Pack 2 (SP2) and later</b>. The window is navigating to an untrusted, non-HTML file. If the user attempts to download the file, do not allow the download.



#### SBSP_NOAUTOSELECT

Suppress selection in the history pane.



#### SBSP_WRITENOHISTORY

Write no history of this navigation in the history Shell folder.



#### SBSP_CREATENOHISTORY (0x00100000)

0x00100000. <b>Windows 7 and later</b>.  Do not add a new entry to the travel log.  When the user enters a search term in the search box and subsequently refines the query, the browser navigates forward but does not add an additional travel log entry.



#### SBSP_TRUSTEDFORACTIVEX (0x10000000)

<b>Microsoft Internet Explorer 6 Service Pack 2 (SP2) and later</b>. The navigate should allow ActiveX prompts.



#### SBSP_FEEDNAVIGATION (0x20000000)

<b>Windows Internet Explorer 7 and later</b>. If allowed by current registry settings, give the browser a destination to navigate to.





#### SBSP_REDIRECT (0x40000000)

Enables redirection to another URL.



#### SBSP_INITIATEDBYHLINKFRAME (0x80000000)



#### SBSP_PLAYNOSOUND (0x00200000)

<b>Windows 7 and later</b>.  Do not make the navigation complete sound for each keystroke in the search box.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Views can use this method to force Windows Explorer to browse to a specific place in the namespace. Typically, these are folders contained in the view.


#### Examples




```cpp
IShellBrowser* psb;
hr = IUnknown_QueryService(punkSite, SID_STopLevelBrowser, IID_PPV_ARGS(&psb));

if (SUCCEEDED(hr))
{
    hr = psb->BrowseObject(pidlSearch, SBSP_DEFBROWSER | SBSP_ABSOLUTE);
    psb->Release();
}
```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a>