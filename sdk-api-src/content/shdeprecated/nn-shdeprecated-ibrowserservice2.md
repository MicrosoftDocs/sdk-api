---
UID: NN:shdeprecated.IBrowserService2
title: IBrowserService2 (shdeprecated.h)
author: windows-sdk-content
description: Deprecated.
old-location: shell\IBrowserService2.htm
tech.root: shell
ms.assetid: 5c100b60-ef2e-4044-9f06-c1d01bcd88d2
ms.author: windowssdkdev
ms.date: 12/5/2018
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
---

# IBrowserService2 interface


## -description


Deprecated. <b>IBrowserService2</b> extends <a href="https://msdn.microsoft.com/e12ada84-0825-4946-8075-731dfc51ef50">IBrowserService</a>. The methods exposed by this interface are analogous to virtual protected methods in normal C++ inheritance. The objects' inheritance hierarchy spans multiple  DLLs. The hierarchy is made up of a base class and several derived classes that correspond to controls including CLSID_WebBrowser and the user's desktop. Objects not in the hierarchy should not implement this interface or use most of its methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBrowserService2</b> interface inherits from <a href="https://msdn.microsoft.com/e12ada84-0825-4946-8075-731dfc51ef50">IBrowserService</a>. <b>IBrowserService2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/fa3605fe-ebff-48f9-a9d2-9146c719696d">_CancelPendingNavigationAsync</a>
</td>
<td align="left" width="63%">
Deprecated. Enables a derived class to request that the base class cancel any pending navigation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70f1c3b7-be10-44e1-b119-cdae23dde1c1">_CancelPendingView</a>
</td>
<td align="left" width="63%">
Deprecated. Enables a derived class to request that the base class cancel any pending views.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2028fbc6-41e1-4d98-9149-7de6458c5446">_CloseAndReleaseToolbars</a>
</td>
<td align="left" width="63%">
Deprecated. Requests the closing of the browser toolbars hosted by the derived class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e13763de-a3cb-42ea-a3bc-e9324e14d336">_DisableModeless</a>
</td>
<td align="left" width="63%">
Deprecated. Enables a derived class to ask the base class whether a modal UI is visible. A modal UI blocks minimize and close behavior in the browser window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d66274b5-36ca-474c-b0e2-49b34394b19b">_ExecChildren</a>
</td>
<td align="left" width="63%">
Deprecated. Enables the derived class to issue a command through the <a href="https://msdn.microsoft.com/a2071ca9-8675-4f53-b30e-8c7198c2acca">IOleCommandTarget::Exec</a> method directly, instead of relying on the base class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1bf707e5-8849-4b5c-aa5b-f77ccfbc3ad7">_FindTBar</a>
</td>
<td align="left" width="63%">
Deprecated. Returns the index of a browser toolbar item based on COM identity rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/411c55ca-f9c3-4ecc-ac9d-96f23dcf3e39">_get_itbLastFocus</a>
</td>
<td align="left" width="63%">
Deprecated. Gets the ID of the last toolbar or view that had focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44477311-61c6-48d0-bef8-349ca114a891">_GetBorderDWHelper</a>
</td>
<td align="left" width="63%">
Deprecated. A helper method for the implementation of <a href="https://msdn.microsoft.com/b1c30a49-8d87-4855-acc0-5f33eabe5e8a">GetBorderDW</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0c53cd4-4b85-42d5-98c3-22ef46644a3f">_GetEffectiveClientArea</a>
</td>
<td align="left" width="63%">
Deprecated. Used with <a href="https://msdn.microsoft.com/62ede825-a4f3-47bc-a9dd-9b651bde1ec5">IBrowserService2::_GetViewBorderRect</a> to negotiate the dimensions of the browser view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7884c80d-dc15-42a7-80e3-566eed819275">_GetToolbarCount</a>
</td>
<td align="left" width="63%">
Deprecated. Returns the number of toolbars in the browser window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bce71ca-189e-4072-9acf-10c8b3a34c5c">_GetToolbarItem</a>
</td>
<td align="left" width="63%">
Deprecated. Gets a specific item from a toolbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62ede825-a4f3-47bc-a9dd-9b651bde1ec5">_GetViewBorderRect</a>
</td>
<td align="left" width="63%">
Deprecated. Used with <a href="https://msdn.microsoft.com/c0c53cd4-4b85-42d5-98c3-22ef46644a3f">IBrowserService2::_GetEffectiveClientArea</a> to negotiate the size and position of the browser view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/990f7456-dce3-4c67-9a1e-97c8772e4332">_Initialize</a>
</td>
<td align="left" width="63%">
Deprecated. Coordinates the initializing of state between the base and the derived classes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3dd5b22-8834-4601-b91b-d5c4ded01549">_LoadToolbars</a>
</td>
<td align="left" width="63%">
Deprecated. Loads the saved state of the browser's toolbars.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f75f4d7-5bb3-4fc4-aefa-32e52d1ab85e">_MaySaveChanges</a>
</td>
<td align="left" width="63%">
Deprecated. Enables the base class to check whether the browser view needs to save changes before closing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71f99bc7-0601-4dc4-90df-c9f9a0ab51a5">_NavigateToPidl</a>
</td>
<td align="left" width="63%">
Deprecated. Navigates the base class to a new location synchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/724b6f35-c419-4b67-bffd-c509e54715d0">_OnFocusChange</a>
</td>
<td align="left" width="63%">
Deprecated. Coordinates focus between the base and the derived class when the focus shifts between the derived class's browser toolbars and its view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc6884c8-222c-4990-b178-ea5665d30d57">_PauseOrResumeView</a>
</td>
<td align="left" width="63%">
Deprecated. Enables a derived class to request the base class to either pause (such as before a minimize operation) or resume the browser view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08b67fad-1c9d-46b6-81dd-d77721448bc6">_put_itbLastFocus</a>
</td>
<td align="left" width="63%">
Deprecated. Sets the last toolbar or the last view with focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d7c618a-2948-44cf-8e47-96d33c08c9a5">_ResizeNextBorder</a>
</td>
<td align="left" width="63%">
Deprecated. Resizes the border of the browser view in response to the addition or removal of toolbars.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/850025c0-96a0-4b7b-aa87-18325b0aecab">_ResizeNextBorderHelper</a>
</td>
<td align="left" width="63%">
Deprecated. A helper method used by the implementation of <a href="https://msdn.microsoft.com/9d7c618a-2948-44cf-8e47-96d33c08c9a5">IBrowserService2::_ResizeNextBorder</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12b38906-f22a-490d-9b2f-192eb43a8305">_ResizeView</a>
</td>
<td align="left" width="63%">
Deprecated. Calls <a href="https://msdn.microsoft.com/92860c13-cb67-4499-90fe-2b0254ae25c7">IBrowserService2::_UpdateViewRectSize</a>, then updates the browser view by using <a href="https://msdn.microsoft.com/240d2ae5-abce-4bea-969e-f47780908bbb">IOleInPlaceActiveObject::ResizeBorder</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d05ed3d-13a3-49a2-8248-9976bc492b0f">_SaveToolbars</a>
</td>
<td align="left" width="63%">
Deprecated. Saves the state of browser toolbars.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/159516ce-1731-478a-8d84-85d0001f9c63">_SendChildren</a>
</td>
<td align="left" width="63%">
Deprecated. Allows the derived class to send a message through the <a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a> function directly instead of relying on the base class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a69c3f4-49e0-4a06-8cf2-dc8db640f58f">_SetFocus</a>
</td>
<td align="left" width="63%">
Deprecated. Sets the focus on a toolbar or on the browser's view window. Called when translating accelerators through <a href="https://msdn.microsoft.com/dda5c085-7199-4b83-b03e-e4c715665157">TranslateAcceleratorSB</a> or when <a href="https://msdn.microsoft.com/a1c271b2-d567-43b4-966e-0eea597f004b">IBrowserService2::v_MayGetNextToolbarFocus</a> fails.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e0a74cf-e554-4be4-8221-5a64addff12d">_SwitchActivationNow</a>
</td>
<td align="left" width="63%">
Deprecated. Coordinates state updates while switching between current and pending browser views.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30801c5d-151b-4556-a1e5-1cbc81a5c33a">_TryShell2Rename</a>
</td>
<td align="left" width="63%">
Deprecated. Coordinates the renaming of the current browser view when the browser is redirected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c8439f8-5931-4aca-8085-2707b6f964f0">_UIActivateView</a>
</td>
<td align="left" width="63%">
Deprecated. Allows a derived class to request that the base class update the browser view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92860c13-cb67-4499-90fe-2b0254ae25c7">_UpdateViewRectSize</a>
</td>
<td align="left" width="63%">
Deprecated. Called to inform other functions involved in the browser view size negotiations that the allowable browser view dimensions have changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/833acb3f-4c33-4b46-8759-3c08698cd245">ActivatePendingView</a>
</td>
<td align="left" width="63%">
Deprecated. Coordinates state updating while the browser is switching between a current and a pending view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/005d1c7a-00cc-4083-bde6-d3fa947de28e">AllowViewResize</a>
</td>
<td align="left" width="63%">
Deprecated. Informs the base class whether to allow view resizing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2738e62b-5577-416b-952e-18a189fc717f">CreateBrowserPropSheetExt</a>
</td>
<td align="left" width="63%">
Deprecated. Allows the derived class to add <b>Folder Options</b> property sheets to the base class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5e7f18b-86b3-4a30-bbb0-8c7f615c7186">CreateViewWindow</a>
</td>
<td align="left" width="63%">
Deprecated. Coordinates the updating of state when creating a new browser view window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8db9fbf9-9132-47a4-a788-93c303598ba0">ForwardViewMsg</a>
</td>
<td align="left" width="63%">
Deprecated. Calls the <a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a> function with a message received by the view, using the <b>_hwndView</b> member of the <a href="https://msdn.microsoft.com/d56e42e8-a556-4470-82d9-466edd84214f">BASEBROWSERDATA</a> structure as the <b>SendMessage</b>
<i>hWnd</i> parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60a9bbd1-5c11-4c6a-bae2-b85979ab8bda">GetBaseBrowserData</a>
</td>
<td align="left" width="63%">
Deprecated. Gets a read-only structure containing the protected elements owned by the base class, for the purpose of determining state.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fac9323b-bf32-45d0-95c4-798a1aab4d02">GetFolderSetData</a>
</td>
<td align="left" width="63%">
Deprecated. Gets a structure containing folder information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/738aa84d-9586-493e-8a50-e8e1918198e6">GetViewRect</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves a value that is used to negotiate the allowed size of the window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec0b2304-cbcb-49ac-aca0-780f1e5205ad">GetViewWindow</a>
</td>
<td align="left" width="63%">
Deprecated. Provides direct access to the browser view window created by <a href="https://msdn.microsoft.com/f5e7f18b-86b3-4a30-bbb0-8c7f615c7186">IBrowserService2::CreateViewWindow</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b217d5cd-c9db-4d35-96de-25e1ec22670a">InitializeDownloadManager</a>
</td>
<td align="left" width="63%">
Deprecated. Enables the download manager in the base class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8bb2efc6-699f-4e12-bb52-ee15fb8dc85a">InitializeTransitionSite</a>
</td>
<td align="left" width="63%">
Deprecated. Enables transitions in the browser view window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff2165da-e195-4cc1-ba89-c11eb37ac4c3">InitializeTravelLog</a>
</td>
<td align="left" width="63%">
Deprecated. Allows the derived class to specify a navigation record to be used in a new window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1f4a4bd-2fd8-424f-b84a-d68b7e2e019c">Offline</a>
</td>
<td align="left" width="63%">
Deprecated. Checks for and updates the browser's offline status, synchronzing the state between the base class and any derived classes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2bffddc0-9e29-4d38-ae02-c9b1e5dc2c36">OnCommand</a>
</td>
<td align="left" width="63%">
Deprecated. Calls the derived class from the base class on receipt of a <a href="https://msdn.microsoft.com/en-us/library/ms647591(v=VS.85).aspx">WM_COMMAND</a> message. The derived class handles the message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abfcb67a-c383-4480-9da9-788fb9cebf5e">OnCreate</a>
</td>
<td align="left" width="63%">
Deprecated. Calls the derived class from the base class on receipt of a <a href="https://msdn.microsoft.com/en-us/library/ms632619(v=VS.85).aspx">WM_CREATE</a> message. The derived class handles the message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/103456a8-d4d1-46f7-b002-a8daa166db29">OnDestroy</a>
</td>
<td align="left" width="63%">
Deprecated. Calls the derived class from the base class on receipt of a <a href="https://msdn.microsoft.com/en-us/library/ms632620(v=VS.85).aspx">WM_DESTROY</a> message. The derived class handles the message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02134f59-c162-4247-9508-7ba40eec388b">OnFrameWindowActivateBS</a>
</td>
<td align="left" width="63%">
Deprecated. Calls the derived class from the base class in response to a subframe window being activated or deactivated. The derived class determines what to do in response to the action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/666d76da-0891-4645-8852-fc963be75369">OnNotify</a>
</td>
<td align="left" width="63%">
Deprecated. Calls the derived class from the base class on receipt of a <a href="https://msdn.microsoft.com/en-us/library/Bb775583(v=VS.85).aspx">WM_NOTIFY</a> message. The derived class handles the message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/107a2ce8-2914-423a-bda7-4aeb112965bc">OnSetFocus</a>
</td>
<td align="left" width="63%">
Deprecated. Calls the derived class from the base class on receipt of a <a href="https://msdn.microsoft.com/en-us/library/ms646283(v=VS.85).aspx">WM_SETFOCUS</a> message. The derived class handles the message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/082eabc4-6807-4d40-aa06-f7d230039073">OnSize</a>
</td>
<td align="left" width="63%">
Deprecated. Calls the derived class from the base class on receipt of a <a href="https://msdn.microsoft.com/en-us/library/ms632646(v=VS.85).aspx">WM_SIZE</a> message. The derived class handles the message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/960bcc2c-9c2c-47e7-ad32-27dcdc4ad783">PutBaseBrowserData</a>
</td>
<td align="left" width="63%">
Deprecated. Gets a structure that allows read/write access to protected members of the base class. Note, however, that state should only be updated by the base browser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/722aee91-6a30-4818-95aa-ecb88b5ef215">ReleaseShellView</a>
</td>
<td align="left" width="63%">
Deprecated. Coordinates the view lifetime between the base class and its derived class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64c7ce89-c3c5-4a09-aff2-57103ade671a">SetAcceleratorMenu</a>
</td>
<td align="left" width="63%">
Deprecated. Implemented by a derived class to define menu accelerators that can be used in a call to <a href="https://msdn.microsoft.com/dda5c085-7199-4b83-b03e-e4c715665157">TranslateAcceleratorSB</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a822b69-892d-48dc-99b3-8d725036722d">SetActivateState</a>
</td>
<td align="left" width="63%">
Deprecated. Updates the value of the <b>_uActivateState</b> member of the <a href="https://msdn.microsoft.com/d56e42e8-a556-4470-82d9-466edd84214f">BASEBROWSERDATA</a> structure, which tracks whether the browser view window is in an activated state. The derived class makes this call to the base class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5bcbb41-7c43-4448-a612-fe2342c502a0">SetAsDefFolderSettings</a>
</td>
<td align="left" width="63%">
Deprecated. Sets the folder's current view mode as the default view mode for all folders. Used by the <b>Folder Options</b> dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e230d832-c57b-4c4a-8da6-a56bf7fe58c9">SetTopBrowser</a>
</td>
<td align="left" width="63%">
Deprecated. Informs the base class when it becomes the topmost browser instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a24244d-197e-4df4-bcd9-546c999b2534">UpdateSecureLockIcon</a>
</td>
<td align="left" width="63%">
Deprecated. Updates the value of the <b>_eSecureLockIcon</b> member of the <a href="https://msdn.microsoft.com/d56e42e8-a556-4470-82d9-466edd84214f">BASEBROWSERDATA</a> structure, which tracks the icon indicating a secure site, as well as updating the icon itself in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc682057-9a84-4b14-bfe3-32b6ada9304c">v_CheckZoneCrossing</a>
</td>
<td align="left" width="63%">
Deprecated. Called by the base class to validate a zone crossing when navigating from one page to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb6b2739-7eb1-4037-8a21-1c4d0f70cde3">v_GetViewStream</a>
</td>
<td align="left" width="63%">
Deprecated. Returns a stream used to load or save the view state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1c271b2-d567-43b4-966e-0eea597f004b">v_MayGetNextToolbarFocus</a>
</td>
<td align="left" width="63%">
Deprecated. Used when translating accelerators through <a href="https://msdn.microsoft.com/dda5c085-7199-4b83-b03e-e4c715665157">TranslateAcceleratorSB</a> and in checking the cycle of focus between the view and the browser's toolbars.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99dc3bce-c661-4233-8457-0ce29e02c270">v_MayTranslateAccelerator</a>
</td>
<td align="left" width="63%">
Deprecated. Called by a derived class to instruct the base class to proceed with the translation of keyboard mnemonics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b97116f7-d42e-4619-bc5b-0a55ac012f0c">v_ShowHideChildWindows</a>
</td>
<td align="left" width="63%">
Deprecated. Allows a derived class to update its child windows after a sizing event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d45877ac-2f0b-4130-9197-83f6e366ee19">WndProcBS</a>
</td>
<td align="left" width="63%">
Deprecated. Allows a derived class to call the <b>WinProc</b> function of the base class.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/e12ada84-0825-4946-8075-731dfc51ef50">IBrowserService</a> interface, from which it inherits.



