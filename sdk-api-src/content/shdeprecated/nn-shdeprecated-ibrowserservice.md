---
UID: NN:shdeprecated.IBrowserService
title: IBrowserService (shdeprecated.h)
description: Deprecated.
helpviewer_keywords: ["IBrowserService","IBrowserService interface [Windows Shell]","IBrowserService interface [Windows Shell]","described","shdeprecated/IBrowserService","shell.IBrowserService","zone_IBrowserService"]
old-location: shell\IBrowserService.htm
tech.root: shell
ms.assetid: e12ada84-0825-4946-8075-731dfc51ef50
ms.date: 12/05/2018
ms.keywords: IBrowserService, IBrowserService interface [Windows Shell], IBrowserService interface [Windows Shell],described, shdeprecated/IBrowserService, shell.IBrowserService, zone_IBrowserService
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService
 - shdeprecated/IBrowserService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService
---

# IBrowserService interface


## -description

Deprecated. The methods exposed by this interface are analogous to virtual protected methods in normal C++ inheritance. The objects' inheritance hierarchy spans multiple DLLs. The hierarchy is made up of a base class and several derived classes that correspond to controls, including CLSID_WebBrowser and the user's desktop. Objects not in the hierarchy should not implement this interface or use most of its methods.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBrowserService</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBrowserService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBrowserService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-cacheoleserver">CacheOLEServer</a>
</td>
<td align="left" width="63%">
Deprecated. Caches a reference to an external object to avoid reloading the server on reuse.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-cannavigatenow">CanNavigateNow</a>
</td>
<td align="left" width="63%">
Deprecated. Returns a value that indicates whether navigation is currently allowed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-displayparseerror">DisplayParseError</a>
</td>
<td align="left" width="63%">
Deprecated. Displays a URL that failed to be successfully parsed by <a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-ieparsedisplayname">IBrowserService::IEParseDisplayName</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-getbrowserbyindex">GetBrowserByIndex</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the browser with the given index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-getbrowserindex">GetBrowserIndex</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the index of the browser in the window hierarchy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the current set of browser flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-gethistoryobject">GetHistoryObject</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> that represents the browser's history object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-getnavigatestate">GetNavigateState</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the browser's current navigation state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-getoleobject">GetOleObject</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> for the browser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-getpalette">GetPalette</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the browser's palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-getparentsite">GetParentSite</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the browser parent's in-place client site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-getpidl">GetPidl</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves a copy of the current PIDL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-getsetcodepage">GetSetCodePage</a>
</td>
<td align="left" width="63%">
Deprecated. Sets a new character code page and retrieves a pointer to the previous code page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-gettitle">GetTitle</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the title of a browser window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-gettravellog">GetTravelLog</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the browser's <a href="/windows/desktop/api/shdeprecated/nn-shdeprecated-itravellog">ITravelLog</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-iegetdisplayname">IEGetDisplayName</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the URL that corresponds to a PIDL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-ieparsedisplayname">IEParseDisplayName</a>
</td>
<td align="left" width="63%">
Deprecated. Parses a URL into a PIDL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-iscontrolwindowshown">IsControlWindowShown</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves a value that indicates whether a specified frame control is currently visible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-navigatetopidl">NavigateToPidl</a>
</td>
<td align="left" width="63%">
Deprecated. Navigates the browser to the location indicated by a PIDL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-notifyredirect">NotifyRedirect</a>
</td>
<td align="left" width="63%">
Deprecated. Updates the browser to the specified PIDL, navigating if necessary. This method is called when a page is redirected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-onhttpequiv">OnHttpEquiv</a>
</td>
<td align="left" width="63%">
Deprecated. Called when the document object responds to an <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes">HTTP-EQUIV</a> metatag by issuing either the <b>OLECMDID_HTTPEQUIV</b> or <b>OLECMDID_HTTPEQUIV_DONE</b> command through <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-exec">IOleCommandTarget::Exec</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-registerwindow">RegisterWindow</a>
</td>
<td align="left" width="63%">
Deprecated. Registers the browser in the list of browser windows.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-setflags">SetFlags</a>
</td>
<td align="left" width="63%">
Deprecated. Sets flags that indicate browser status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-sethistoryobject">SetHistoryObject</a>
</td>
<td align="left" width="63%">
Deprecated. Sets the browser's history object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-setnavigatestate">SetNavigateState</a>
</td>
<td align="left" width="63%">
Deprecated. Sets the current navigation state. This method affects the cursor and animation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-setreferrer">SetReferrer</a>
</td>
<td align="left" width="63%">
Deprecated. Sets the PIDL used for zone checking when creating a new window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-settitle">SetTitle</a>
</td>
<td align="left" width="63%">
Deprecated. Sets the title of a browser window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-showcontrolwindow">ShowControlWindow</a>
</td>
<td align="left" width="63%">
Deprecated. Shows or hides various frame controls.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-updatebackforwardstate">UpdateBackForwardState</a>
</td>
<td align="left" width="63%">
Deprecated. Updates the state of the browser's <b>Back</b> and <b>Forward</b> buttons.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-updatewindowlist">UpdateWindowList</a>
</td>
<td align="left" width="63%">
Deprecated. Instructs the browser to update the PIDL in the window list. This method is called after navigation.

</td>
</tr>
</table>

## -remarks

In a direct inheritance scheme, these methods would be protected members. For that reason, it is recommended that this interface not be used directly by implementers. If it is used directly, existing data could be at risk.