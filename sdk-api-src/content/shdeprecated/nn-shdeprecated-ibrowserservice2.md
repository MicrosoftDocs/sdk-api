---
UID: NN:shdeprecated.IBrowserService2
title: IBrowserService2 (shdeprecated.h)
author: windows-sdk-content
description: Deprecated.
old-location: shell\IBrowserService2.htm
tech.root: shell
ms.assetid: 5c100b60-ef2e-4044-9f06-c1d01bcd88d2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBrowserService2, IBrowserService2 interface [Windows Shell], IBrowserService2 interface [Windows Shell],described, shdeprecated/IBrowserService2, shell.IBrowserService2, zone_IBrowserService2
ms.topic: interface
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
 - Shdeprecated.h
api_name:
 - IBrowserService2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
ms.custom: 19H1
---

# IBrowserService2 interface


## -description


Deprecated. <b>IBrowserService2</b> extends <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nn-shdeprecated-ibrowserservice">IBrowserService</a>. The methods exposed by this interface are analogous to virtual protected methods in normal C++ inheritance. The objects' inheritance hierarchy spans multiple  DLLs. The hierarchy is made up of a base class and several derived classes that correspond to controls including CLSID_WebBrowser and the user's desktop. Objects not in the hierarchy should not implement this interface or use most of its methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBrowserService2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nn-shdeprecated-ibrowserservice">IBrowserService</a>. <b>IBrowserService2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBrowserService2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_cancelpendingnavigationasync">_CancelPendingNavigationAsync</a>
</td>
<td align="left" width="63%">
Deprecated. Enables a derived class to request that the base class cancel any pending navigation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_cancelpendingview">_CancelPendingView</a>
</td>
<td align="left" width="63%">
Deprecated. Enables a derived class to request that the base class cancel any pending views.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_closeandreleasetoolbars">_CloseAndReleaseToolbars</a>
</td>
<td align="left" width="63%">
Deprecated. Requests the closing of the browser toolbars hosted by the derived class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_disablemodeless">_DisableModeless</a>
</td>
<td align="left" width="63%">
Deprecated. Enables a derived class to ask the base class whether a modal UI is visible. A modal UI blocks minimize and close behavior in the browser window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_execchildren">_ExecChildren</a>
</td>
<td align="left" width="63%">
Deprecated. Enables the derived class to issue a command through the <a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-exec">IOleCommandTarget::Exec</a> method directly, instead of relying on the base class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_findtbar">_FindTBar</a>
</td>
<td align="left" width="63%">
Deprecated. Returns the index of a browser toolbar item based on COM identity rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_get_itblastfocus">_get_itbLastFocus</a>
</td>
<td align="left" width="63%">
Deprecated. Gets the ID of the last toolbar or view that had focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_getborderdwhelper">_GetBorderDWHelper</a>
</td>
<td align="left" width="63%">
Deprecated. A helper method for the implementation of <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-idockingwindowsite-getborderdw">GetBorderDW</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_geteffectiveclientarea">_GetEffectiveClientArea</a>
</td>
<td align="left" width="63%">
Deprecated. Used with <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_getviewborderrect">IBrowserService2::_GetViewBorderRect</a> to negotiate the dimensions of the browser view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_gettoolbarcount">_GetToolbarCount</a>
</td>
<td align="left" width="63%">
Deprecated. Returns the number of toolbars in the browser window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_gettoolbaritem">_GetToolbarItem</a>
</td>
<td align="left" width="63%">
Deprecated. Gets a specific item from a toolbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_getviewborderrect">_GetViewBorderRect</a>
</td>
<td align="left" width="63%">
Deprecated. Used with <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_geteffectiveclientarea">IBrowserService2::_GetEffectiveClientArea</a> to negotiate the size and position of the browser view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_initialize">_Initialize</a>
</td>
<td align="left" width="63%">
Deprecated. Coordinates the initializing of state between the base and the derived classes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_loadtoolbars">_LoadToolbars</a>
</td>
<td align="left" width="63%">
Deprecated. Loads the saved state of the browser's toolbars.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_maysavechanges">_MaySaveChanges</a>
</td>
<td align="left" width="63%">
Deprecated. Enables the base class to check whether the browser view needs to save changes before closing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_navigatetopidl">_NavigateToPidl</a>
</td>
<td align="left" width="63%">
Deprecated. Navigates the base class to a new location synchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_onfocuschange">_OnFocusChange</a>
</td>
<td align="left" width="63%">
Deprecated. Coordinates focus between the base and the derived class when the focus shifts between the derived class's browser toolbars and its view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_pauseorresumeview">_PauseOrResumeView</a>
</td>
<td align="left" width="63%">
Deprecated. Enables a derived class to request the base class to either pause (such as before a minimize operation) or resume the browser view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_put_itblastfocus">_put_itbLastFocus</a>
</td>
<td align="left" width="63%">
Deprecated. Sets the last toolbar or the last view with focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_resizenextborder">_ResizeNextBorder</a>
</td>
<td align="left" width="63%">
Deprecated. Resizes the border of the browser view in response to the addition or removal of toolbars.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_resizenextborderhelper">_ResizeNextBorderHelper</a>
</td>
<td align="left" width="63%">
Deprecated. A helper method used by the implementation of <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_resizenextborder">IBrowserService2::_ResizeNextBorder</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_resizeview">_ResizeView</a>
</td>
<td align="left" width="63%">
Deprecated. Calls <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_updateviewrectsize">IBrowserService2::_UpdateViewRectSize</a>, then updates the browser view by using <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceactiveobject-resizeborder">IOleInPlaceActiveObject::ResizeBorder</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_savetoolbars">_SaveToolbars</a>
</td>
<td align="left" width="63%">
Deprecated. Saves the state of browser toolbars.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_sendchildren">_SendChildren</a>
</td>
<td align="left" width="63%">
Deprecated. Allows the derived class to send a message through the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> function directly instead of relying on the base class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_setfocus">_SetFocus</a>
</td>
<td align="left" width="63%">
Deprecated. Sets the focus on a toolbar or on the browser's view window. Called when translating accelerators through <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-translateacceleratorsb">TranslateAcceleratorSB</a> or when <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-v_maygetnexttoolbarfocus">IBrowserService2::v_MayGetNextToolbarFocus</a> fails.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_switchactivationnow">_SwitchActivationNow</a>
</td>
<td align="left" width="63%">
Deprecated. Coordinates state updates while switching between current and pending browser views.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_tryshell2rename">_TryShell2Rename</a>
</td>
<td align="left" width="63%">
Deprecated. Coordinates the renaming of the current browser view when the browser is redirected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_uiactivateview">_UIActivateView</a>
</td>
<td align="left" width="63%">
Deprecated. Allows a derived class to request that the base class update the browser view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_updateviewrectsize">_UpdateViewRectSize</a>
</td>
<td align="left" width="63%">
Deprecated. Called to inform other functions involved in the browser view size negotiations that the allowable browser view dimensions have changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-activatependingview">ActivatePendingView</a>
</td>
<td align="left" width="63%">
Deprecated. Coordinates state updating while the browser is switching between a current and a pending view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-allowviewresize">AllowViewResize</a>
</td>
<td align="left" width="63%">
Deprecated. Informs the base class whether to allow view resizing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-createbrowserpropsheetext">CreateBrowserPropSheetExt</a>
</td>
<td align="left" width="63%">
Deprecated. Allows the derived class to add <b>Folder Options</b> property sheets to the base class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-createviewwindow">CreateViewWindow</a>
</td>
<td align="left" width="63%">
Deprecated. Coordinates the updating of state when creating a new browser view window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-forwardviewmsg">ForwardViewMsg</a>
</td>
<td align="left" width="63%">
Deprecated. Calls the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> function with a message received by the view, using the <b>_hwndView</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/ns-shdeprecated-basebrowserdatalh">BASEBROWSERDATA</a> structure as the <b>SendMessage</b>
<i>hWnd</i> parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-getbasebrowserdata">GetBaseBrowserData</a>
</td>
<td align="left" width="63%">
Deprecated. Gets a read-only structure containing the protected elements owned by the base class, for the purpose of determining state.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-getfoldersetdata">GetFolderSetData</a>
</td>
<td align="left" width="63%">
Deprecated. Gets a structure containing folder information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-getviewrect">GetViewRect</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves a value that is used to negotiate the allowed size of the window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-getviewwindow">GetViewWindow</a>
</td>
<td align="left" width="63%">
Deprecated. Provides direct access to the browser view window created by <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-createviewwindow">IBrowserService2::CreateViewWindow</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-initializedownloadmanager">InitializeDownloadManager</a>
</td>
<td align="left" width="63%">
Deprecated. Enables the download manager in the base class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-initializetransitionsite">InitializeTransitionSite</a>
</td>
<td align="left" width="63%">
Deprecated. Enables transitions in the browser view window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-initializetravellog">InitializeTravelLog</a>
</td>
<td align="left" width="63%">
Deprecated. Allows the derived class to specify a navigation record to be used in a new window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-offline">Offline</a>
</td>
<td align="left" width="63%">
Deprecated. Checks for and updates the browser's offline status, synchronzing the state between the base class and any derived classes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-oncommand">OnCommand</a>
</td>
<td align="left" width="63%">
Deprecated. Calls the derived class from the base class on receipt of a <a href="https://docs.microsoft.com/windows/desktop/menurc/wm-command">WM_COMMAND</a> message. The derived class handles the message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-oncreate">OnCreate</a>
</td>
<td align="left" width="63%">
Deprecated. Calls the derived class from the base class on receipt of a <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-create">WM_CREATE</a> message. The derived class handles the message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-ondestroy">OnDestroy</a>
</td>
<td align="left" width="63%">
Deprecated. Calls the derived class from the base class on receipt of a <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-destroy">WM_DESTROY</a> message. The derived class handles the message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-onframewindowactivatebs">OnFrameWindowActivateBS</a>
</td>
<td align="left" width="63%">
Deprecated. Calls the derived class from the base class in response to a subframe window being activated or deactivated. The derived class determines what to do in response to the action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-onnotify">OnNotify</a>
</td>
<td align="left" width="63%">
Deprecated. Calls the derived class from the base class on receipt of a <a href="https://docs.microsoft.com/windows/desktop/Controls/wm-notify">WM_NOTIFY</a> message. The derived class handles the message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-onsetfocus">OnSetFocus</a>
</td>
<td align="left" width="63%">
Deprecated. Calls the derived class from the base class on receipt of a <a href="https://docs.microsoft.com/windows/desktop/inputdev/wm-setfocus">WM_SETFOCUS</a> message. The derived class handles the message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-onsize">OnSize</a>
</td>
<td align="left" width="63%">
Deprecated. Calls the derived class from the base class on receipt of a <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-size">WM_SIZE</a> message. The derived class handles the message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-putbasebrowserdata">PutBaseBrowserData</a>
</td>
<td align="left" width="63%">
Deprecated. Gets a structure that allows read/write access to protected members of the base class. Note, however, that state should only be updated by the base browser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-releaseshellview">ReleaseShellView</a>
</td>
<td align="left" width="63%">
Deprecated. Coordinates the view lifetime between the base class and its derived class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-setacceleratormenu">SetAcceleratorMenu</a>
</td>
<td align="left" width="63%">
Deprecated. Implemented by a derived class to define menu accelerators that can be used in a call to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-translateacceleratorsb">TranslateAcceleratorSB</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-setactivatestate">SetActivateState</a>
</td>
<td align="left" width="63%">
Deprecated. Updates the value of the <b>_uActivateState</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/ns-shdeprecated-basebrowserdatalh">BASEBROWSERDATA</a> structure, which tracks whether the browser view window is in an activated state. The derived class makes this call to the base class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-setasdeffoldersettings">SetAsDefFolderSettings</a>
</td>
<td align="left" width="63%">
Deprecated. Sets the folder's current view mode as the default view mode for all folders. Used by the <b>Folder Options</b> dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-settopbrowser">SetTopBrowser</a>
</td>
<td align="left" width="63%">
Deprecated. Informs the base class when it becomes the topmost browser instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-updatesecurelockicon">UpdateSecureLockIcon</a>
</td>
<td align="left" width="63%">
Deprecated. Updates the value of the <b>_eSecureLockIcon</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/ns-shdeprecated-basebrowserdatalh">BASEBROWSERDATA</a> structure, which tracks the icon indicating a secure site, as well as updating the icon itself in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-v_checkzonecrossing">v_CheckZoneCrossing</a>
</td>
<td align="left" width="63%">
Deprecated. Called by the base class to validate a zone crossing when navigating from one page to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-v_getviewstream">v_GetViewStream</a>
</td>
<td align="left" width="63%">
Deprecated. Returns a stream used to load or save the view state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-v_maygetnexttoolbarfocus">v_MayGetNextToolbarFocus</a>
</td>
<td align="left" width="63%">
Deprecated. Used when translating accelerators through <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-translateacceleratorsb">TranslateAcceleratorSB</a> and in checking the cycle of focus between the view and the browser's toolbars.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-v_maytranslateaccelerator">v_MayTranslateAccelerator</a>
</td>
<td align="left" width="63%">
Deprecated. Called by a derived class to instruct the base class to proceed with the translation of keyboard mnemonics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-v_showhidechildwindows">v_ShowHideChildWindows</a>
</td>
<td align="left" width="63%">
Deprecated. Allows a derived class to update its child windows after a sizing event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-wndprocbs">WndProcBS</a>
</td>
<td align="left" width="63%">
Deprecated. Allows a derived class to call the <b>WinProc</b> function of the base class.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nn-shdeprecated-ibrowserservice">IBrowserService</a> interface, from which it inherits.



