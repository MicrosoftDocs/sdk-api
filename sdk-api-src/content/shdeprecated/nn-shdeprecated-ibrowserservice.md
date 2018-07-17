---
UID: NN:shdeprecated.IBrowserService
title: IBrowserService
author: windows-sdk-content
description: Deprecated.
old-location: shell\IBrowserService.htm
old-project: shell
ms.assetid: e12ada84-0825-4946-8075-731dfc51ef50
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IBrowserService, IBrowserService interface [Windows Shell], IBrowserService interface [Windows Shell],described, shdeprecated/IBrowserService, shell.IBrowserService, zone_IBrowserService
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: BNSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# IBrowserService interface


## -description


Deprecated. The methods exposed by this interface are analogous to virtual protected methods in normal C++ inheritance. The objects' inheritance hierarchy spans multiple DLLs. The hierarchy is made up of a base class and several derived classes that correspond to controls, including CLSID_WebBrowser and the user's desktop. Objects not in the hierarchy should not implement this interface or use most of its methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBrowserService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBrowserService</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8999e7d7-f29d-4fc8-8f1f-7a8e8b8f45e6">CacheOLEServer</a>
</td>
<td align="left" width="63%">
Deprecated. Caches a reference to an external object to avoid reloading the server on reuse.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ff5260f-767b-49b3-bcfd-5d1ff4b3f9f9">CanNavigateNow</a>
</td>
<td align="left" width="63%">
Deprecated. Returns a value that indicates whether navigation is currently allowed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/966fec07-6a67-435a-8908-67999afce9f0">DisplayParseError</a>
</td>
<td align="left" width="63%">
Deprecated. Displays a URL that failed to be successfully parsed by <a href="https://msdn.microsoft.com/02f5a6cb-2f90-4613-80cd-1e8a47bb32c2">IBrowserService::IEParseDisplayName</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/190bd99d-3921-4d7b-8cf3-c91067d3e1f8">GetBrowserByIndex</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the browser with the given index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/293d7641-7858-4aa9-983c-6b25a05930d9">GetBrowserIndex</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the index of the browser in the window hierarchy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546791">GetFlags</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the current set of browser flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/409d76e8-5501-437d-92d3-55e1676a80b8">GetHistoryObject</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves an <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> that represents the browser's history object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a8aac75-3e0b-4ff2-a1ec-e08379e67c84">GetNavigateState</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the browser's current navigation state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ac2346f-3bfb-498f-97c7-77dc431567c7">GetOleObject</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves an <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> for the browser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/039a24d0-8cda-48bf-a10b-baf6d76c808d">GetPalette</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the browser's palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91d031ae-1451-4379-9d8e-baddefd30435">GetParentSite</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the browser parent's in-place client site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49104b30-85c0-4adf-acfc-a06b5c4bbdef">GetPidl</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves a copy of the current PIDL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d194f9a-cf82-47ed-8218-d0d5824be435">GetSetCodePage</a>
</td>
<td align="left" width="63%">
Deprecated. Sets a new character code page and retrieves a pointer to the previous code page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5b514e3-8729-4902-961f-177dc1e77aee">GetTitle</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the title of a browser window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e6c09e4-5489-4c21-8e42-28cdc4c216f1">GetTravelLog</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the browser's <a href="https://msdn.microsoft.com/820869aa-ca93-4bb5-831a-3afb52da5389">ITravelLog</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/012d794a-9823-4af2-b628-ad33a93dbbb5">IEGetDisplayName</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves the URL that corresponds to a PIDL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02f5a6cb-2f90-4613-80cd-1e8a47bb32c2">IEParseDisplayName</a>
</td>
<td align="left" width="63%">
Deprecated. Parses a URL into a PIDL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbbb83ce-be7c-4763-b2c4-2a05a460cbd6">IsControlWindowShown</a>
</td>
<td align="left" width="63%">
Deprecated. Retrieves a value that indicates whether a specified frame control is currently visible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb329a61-1c1a-49c6-9d5e-ccfc7fd8b10c">NavigateToPidl</a>
</td>
<td align="left" width="63%">
Deprecated. Navigates the browser to the location indicated by a PIDL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a37c20b9-e2c6-438b-9fd5-749c680d5ee0">NotifyRedirect</a>
</td>
<td align="left" width="63%">
Deprecated. Updates the browser to the specified PIDL, navigating if necessary. This method is called when a page is redirected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9920c08b-c0c3-4359-9c00-3a1063cea0c7">OnHttpEquiv</a>
</td>
<td align="left" width="63%">
Deprecated. Called when the document object responds to an <a href="_inet_HTTP_EQUIV_Attribute_httpEquiv_Property_scr">HTTP-EQUIV</a> metatag by issuing either the <b>OLECMDID_HTTPEQUIV</b> or <b>OLECMDID_HTTPEQUIV_DONE</b> command through <a href="https://msdn.microsoft.com/a2071ca9-8675-4f53-b30e-8c7198c2acca">IOleCommandTarget::Exec</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39d4c31b-bbe4-4b45-b335-c4ae299b1ae3">RegisterWindow</a>
</td>
<td align="left" width="63%">
Deprecated. Registers the browser in the list of browser windows.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556703">SetFlags</a>
</td>
<td align="left" width="63%">
Deprecated. Sets flags that indicate browser status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a0b55b0-a6b6-4b0c-be09-cfb573a5420c">SetHistoryObject</a>
</td>
<td align="left" width="63%">
Deprecated. Sets the browser's history object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cdbe902-f208-43f8-9019-d61c22635196">SetNavigateState</a>
</td>
<td align="left" width="63%">
Deprecated. Sets the current navigation state. This method affects the cursor and animation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6458f28c-4eab-45dc-bc99-24e5f9ea3553">SetReferrer</a>
</td>
<td align="left" width="63%">
Deprecated. Sets the PIDL used for zone checking when creating a new window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/236f05a3-d31b-46fe-9e10-1f5df6823fa3">SetTitle</a>
</td>
<td align="left" width="63%">
Deprecated. Sets the title of a browser window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11ded544-6fba-41a5-bc61-222467fdbc05">ShowControlWindow</a>
</td>
<td align="left" width="63%">
Deprecated. Shows or hides various frame controls.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03e4a470-96dc-408c-a124-5230c185b075">UpdateBackForwardState</a>
</td>
<td align="left" width="63%">
Deprecated. Updates the state of the browser's <b>Back</b> and <b>Forward</b> buttons.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c82a486-f8ad-4868-80ab-ae4a2ebcc95f">UpdateWindowList</a>
</td>
<td align="left" width="63%">
Deprecated. Instructs the browser to update the PIDL in the window list. This method is called after navigation.

</td>
</tr>
</table> 


## -remarks



In a direct inheritance scheme, these methods would be protected members. For that reason, it is recommended that this interface not be used directly by implementers. If it is used directly, existing data could be at risk.



