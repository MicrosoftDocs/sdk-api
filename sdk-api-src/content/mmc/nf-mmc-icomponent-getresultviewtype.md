---
UID: NF:mmc.IComponent.GetResultViewType
title: IComponent::GetResultViewType (mmc.h)
description: The IComponent::GetResultViewType method determines what the result pane view should be.
helpviewer_keywords: ["GetResultViewType","GetResultViewType method [MMC]","GetResultViewType method [MMC]","IComponent interface","IComponent interface [MMC]","GetResultViewType method","IComponent.GetResultViewType","IComponent::GetResultViewType","MMC_VIEW_OPTIONS_CREATENEW","MMC_VIEW_OPTIONS_EXCLUDE_SCOPE_ITEMS_FROM_LIST","MMC_VIEW_OPTIONS_FILTERED","MMC_VIEW_OPTIONS_LEXICAL_SORT","MMC_VIEW_OPTIONS_MULTISELECT","MMC_VIEW_OPTIONS_NOLISTVIEWS","MMC_VIEW_OPTIONS_NONE","MMC_VIEW_OPTIONS_OWNERDATALIST","MMC_VIEW_OPTIONS_USEFONTLINKING","_slate_icomponent_getresultviewtype","mmc.icomponent_getresultviewtype","mmc/IComponent::GetResultViewType"]
old-location: mmc\icomponent_getresultviewtype.htm
tech.root: mmc
ms.assetid: d2575f79-d646-41b5-84a5-768402cfb826
ms.date: 12/05/2018
ms.keywords: GetResultViewType, GetResultViewType method [MMC], GetResultViewType method [MMC],IComponent interface, IComponent interface [MMC],GetResultViewType method, IComponent.GetResultViewType, IComponent::GetResultViewType, MMC_VIEW_OPTIONS_CREATENEW, MMC_VIEW_OPTIONS_EXCLUDE_SCOPE_ITEMS_FROM_LIST, MMC_VIEW_OPTIONS_FILTERED, MMC_VIEW_OPTIONS_LEXICAL_SORT, MMC_VIEW_OPTIONS_MULTISELECT, MMC_VIEW_OPTIONS_NOLISTVIEWS, MMC_VIEW_OPTIONS_NONE, MMC_VIEW_OPTIONS_OWNERDATALIST, MMC_VIEW_OPTIONS_USEFONTLINKING, _slate_icomponent_getresultviewtype, mmc.icomponent_getresultviewtype, mmc/IComponent::GetResultViewType
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComponent::GetResultViewType
 - mmc/IComponent::GetResultViewType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IComponent.GetResultViewType
---

# IComponent::GetResultViewType


## -description

The <b>IComponent::GetResultViewType</b> method 
    determines what the result pane view should be.

## -parameters

### -param cookie [in]

A value that specifies the snapin-provided unique identifier for the scope item. For more details about 
      cookies in MMC, see <a href="/previous-versions/windows/desktop/mmc/cookies">Cookies</a>.

### -param ppViewType [out]

A pointer to the address of a string that specifies the view to display for the specified 
      <i>cookie</i>. The callee (snap-in) allocates the view type string using the COM API function 
      <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and the caller (MMC) frees it using 
      <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

The string that is returned depends on the view type:





#### Standard list

For standard list views, MMC does not use this value. If the snap-in uses only standard list views, the 
         snap-in can set <i>ppViewType</i> to <b>NULL</b>. MMC uses standard 
         list views as the default view type.



#### Taskpad

For a taskpad view that uses MMC taskpad templates, <i>ppViewType</i> should point to 
          the address of a string that contains the resource path to the taskpad template and a group name that 
          identifies the taskpad. Be aware that MMC passes the group name in calls to 
          <a href="/windows/desktop/api/mmc/nn-mmc-iextendtaskpad">IExtendTaskPad</a> methods to enable the snap-in to 
          identify the particular taskpad that is being displayed (this is important if the snap-in has multiple 
          taskpads).

The string should have the following form:

"res://<i>filepath</i>/<i>template</i>#<i>groupname</i>"

where <i>filepath</i> is the full path to the MMC executable 
          (MMC.exe), <i>template</i> is the file name of the template 
          that is stored as a resource within the file specified by <i>filepath</i>, and 
          <i>groupname</i> is the name that identifies the taskpad.

MMC supplies the following HTML files as templates:

<table>
<tr>
<th>Resource file</th>
<th>Description</th>
</tr>
<tr>
<td>default.htm</td>
<td>Template for standard taskpad</td>
</tr>
<tr>
<td>listpad.htm</td>
<td>Template for "vertical" list view taskpad</td>
</tr>
<tr>
<td>horizontal.htm</td>
<td>Template for "horizontal" list view taskpad</td>
</tr>
</table>
 

For example, the following string specifies that MMC.exe has a path of 
          c:\Windows\System32\mmc.exe, the standard taskpad is displayed (default.htm), and 
          the group name is tpad1: "res://c:\\Windows\\System32\\mmc.exe/default.htm#tpad1".

For a taskpad view that uses a custom HTML page, <i>ppViewType</i> should point to the 
          address of a string that contains the resource path to the custom taskpad's HTML file and a group name that 
          identifies the taskpad. The string has the same form as the string for an MMC taskpad 
          template—except the <i>filepath</i> should specify the path to the 
          snap-in's DLL that stores the custom HTML page as a resource.



#### Custom OCX

For a custom view provided by an OLE custom control (OCX), 
          <i>ppViewType</i> should point to the address of a string that contains the string 
          representation of the custom control's <b>CLSID</b>. The string must begin with an 
          open curly brace ({) and end with a close curly brace (}). The following string represents the Calendar 
          control and could be returned in the <i>ppViewType</i> parameter to display the Calendar 
          control in the result pane: "{8E27C92B-1264-101C-8A2F-040224009C02}".

MMC allows a single instance of each OCX type per snap-in instance per view. If the 
          <b>MMC_VIEW_OPTIONS_CREATENEW</b> option is not selected, MMC will display the cached 
          OCX instance for any of the snap-in's scope items that request this OCX view. If 
          the <b>MMC_VIEW_OPTIONS_CREATENEW</b> option is selected, MMC will destroy the cached 
          OCX and create a new one every time a item requests the OCX view.



#### Custom webpage

For a custom view provided by a webpage, <i>ppViewType</i> should point to the 
         address of a string that contains the URL for the page. The following string represents the URL for the 
         Microsoft website and could be returned in the <i>ppViewType</i> parameter to display the 
         website in the result pane: "www.microsoft.com".

### -param pViewOptions [out]

A pointer to the value that provides the console with options specified by the owning snap-in. This value 
      can be a combination of the following:



#### MMC_VIEW_OPTIONS_CREATENEW (0x0010)

For a custom OCX view. In MMC 1.2, the OCX is always cached. If this flag is not 
         specified, MMC 1.2 displays the cached OCX instance for any of the snap-in's scope items that 
         request this OCX view. If this flag is specified, MMC 1.2 destroys the cached OCX 
         and creates (then caches) a new one every time an item requests the OCX view. In MMC 2.0, the 
         OCX will be cached only if this flag is not set. In MMC 2.0, the snap-in can release any 
         OCXs when the node is deselected if this flag is set.

Once the snap-in has specified its OCX caching option for a node (either by using or not using 
         the <b>MMC_VIEW_OPTIONS_CREATENEW</b> flag), it must not change the option choice for this 
         instance of the snap-in.



#### MMC_VIEW_OPTIONS_EXCLUDE_SCOPE_ITEMS_FROM_LIST (0x00000040)

New in MMC 1.2. In a standard list view, this option tells MMC to hide scope items in the view. Scope 
        items are automatically hidden in virtual list views.



#### MMC_VIEW_OPTIONS_FILTERED (0x0008)

Notifies MMC that the snap-in supports filtered views. See 
        <a href="/previous-versions/windows/desktop/mmc/adding-filtered-views">Adding Filtered Views</a>.



#### MMC_VIEW_OPTIONS_LEXICAL_SORT (0x00000080)

New in MMC 1.2. In a standard list view, this option tells MMC to lexically sort all scope items 
        (including extensions) first, followed by all result items. The 
        <a href="/windows/desktop/api/mmc/nn-mmc-iresultdatacompare">IResultDataCompare</a> and 
        <a href="/windows/desktop/api/mmc/nn-mmc-iresultdatacompareex">IResultDataCompareEx</a> interfaces are ignored when 
        this option is set.



#### MMC_VIEW_OPTIONS_MULTISELECT (0x0004)

Allows multiple item selections in the result pane view.



#### MMC_VIEW_OPTIONS_NOLISTVIEWS (0x0001)

Tells the console to refrain from presenting standard list view choices in the 
        <b>View</b> menu. Allows the snap-in to display only its own custom views in the result 
        pane.



#### MMC_VIEW_OPTIONS_NONE (0)

No view options selected. This is the default view option.



#### MMC_VIEW_OPTIONS_OWNERDATALIST (0x0002)

A value that specifies that the result pane list view should be a virtual list.



#### MMC_VIEW_OPTIONS_USEFONTLINKING (0x0020)

Use font linking on result items (for multilingual support). See Remarks for details.

If <i>ppViewType</i> is a custom view type, the view options that affect the standard 
       list views are applied by MMC when the view is switched from a custom view to a standard list view.

## -returns

This method can return one of these values.

## -remarks

The callee (snap-in) allocates the view type string using COM API function 
    <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and the caller (MMC) frees it using 
    <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

MMC calls <b>GetResultViewType</b> when a 
    snap-in scope item is selected. When switching from a standard list view to a custom view, the snap-in must call 
    <a href="/previous-versions/windows/desktop/legacy/aa814792(v=vs.85)">IConsole2::SelectScopeItem</a> to reselect the item 
    and force MMC to call <b>GetResultViewType</b> 
    again. This enables the snap-in to specify the appropriate custom OCX or webpage so that MMC can load 
    it. When switching from a custom view to a standard list view, MMC automatically calls 
    <b>GetResultViewType</b> and sets the appropriate 
    list view type.

Given a Unicode string, the font linking feature determines the best font for that displays that string. For 
    example, if you were populating a list view with server names and knew that half would be in Japanese and half in 
    Russian, then you would set the font linking view options and MMC would determine an appropriate font. The default 
    is not to use font linking, because there is a small performance hit when MMC searches for the appropriate 
    font.

A <a href="/previous-versions/windows/desktop/mmc/cookies">cookie</a> is a pointer to a structure that contains information 
    unique to a specific item. It is passed in through the <b>lParam</b> member of a 
    <a href="/windows/desktop/api/mmc/ns-mmc-scopedataitem">SCOPEDATAITEM</a> structure.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>