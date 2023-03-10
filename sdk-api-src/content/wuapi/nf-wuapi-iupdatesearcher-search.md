---
UID: NF:wuapi.IUpdateSearcher.Search
title: IUpdateSearcher::Search (wuapi.h)
description: Performs a synchronous search for updates. The search uses the search options that are currently configured.
helpviewer_keywords: ["IUpdateSearcher interface [Windows Update Agent]","Search method","IUpdateSearcher.Search","IUpdateSearcher::Search","Search","Search method [Windows Update Agent]","Search method [Windows Update Agent]","IUpdateSearcher interface","wua.iupdatesearchersearch","wuapi/IUpdateSearcher::Search"]
old-location: wua\iupdatesearchersearch.htm
tech.root: wua
ms.assetid: 0511cfd0-f4de-41ab-af35-32d757217386
ms.date: 12/05/2018
ms.keywords: IUpdateSearcher interface [Windows Update Agent],Search method, IUpdateSearcher.Search, IUpdateSearcher::Search, Search, Search method [Windows Update Agent], Search method [Windows Update Agent],IUpdateSearcher interface, wua.iupdatesearchersearch, wuapi/IUpdateSearcher::Search
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateSearcher::Search
 - wuapi/IUpdateSearcher::Search
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateSearcher.Search
---

# IUpdateSearcher::Search


## -description

Performs a synchronous search for updates. The search uses the search options that are currently configured.

## -parameters

### -param criteria [in]

A string that specifies the search criteria.

### -param retval [out]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-isearchresult">ISearchResult</a> interface that contains the following:

<ul>
<li>The result of an operation</li>
<li>A collection of updates that match the search criteria</li>
</ul>

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_LEGACYSERVER</b></dt>
</dl>
</td>
<td width="60%">
You cannot search for updates if the <a href="/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a">ServerSelection</a> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface is set to <a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/wuapicommon/ne-wuapicommon-serverselection.md">ssManagedServer</a> or <a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/wuapicommon/ne-wuapicommon-serverselection.md">ssDefault</a>, and the managed server on a computer is a Microsoft Software Update Services (SUS) 1.0 server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter value is invalid or <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALID_CRITERIA</b></dt>
</dl>
</td>
<td width="60%">
There is an invalid search criteria.

</td>
</tr>
</table>

## -remarks

The string that is used for the <i>criteria</i> parameter must match the custom search language for the <b>Search</b> method.  The string consists of criteria that are evaluated to determine the updates to return.

Each criterion specifies an update property name and value. With some restrictions, multiple criteria can be connected with the <b>AND</b> and <b>OR</b> operators. The <b>=</b> (equal) and  <b>!=</b> (not-equal) operators are both supported. When you use Windows Update Agent (WUA), the <b>!=</b> (not-equal) operator can be used only with the type criterion.

The search criteria syntax is based on the WHERE clause of an SQL query expression. Most of the supported criteria map directly to update properties. These update properties resemble the elements in a virtual XML document that contains the entire server catalog. For example, if you specify a search criteria string of "AutoSelectOnWebSites = 1", the search returns all the updates that have a AutoSelectOnWebSites property with a value of <b>VARIANT_TRUE</b>.

A single criterion consists of "<i>Name</i> = <i>Value</i>" or "<i>Name</i> != <i>Value</i>", where "<i>Name</i>" is one of the supported criterion names, and "<i>Value</i>" is a string or an integer. The <b>AND</b> and <b>OR</b> operators can be used to connect multiple criteria. However, <b>OR</b> can be used only  at the top level of the search criteria. Therefore, "(x=1 and y=1) or (z=1)" is valid, but "(x=1) and (y=1 or z=1)" is not valid.

The supported value types are integers and strings. An integer must be specified in base 10, and negative numbers are prefixed with a minus sign (<b>-</b>). A string must be escaped and enclosed in single quotation marks ('). All string comparisons are case-insensitive unless specified.

The following table identifies all the public support criteria in the order of evaluation precedence. More criteria may be added to this list in the future.

<table>
<tr>
<th>Criterion</th>
<th>Type</th>
<th>Allowed operators</th>
<th>Description</th>
</tr>
<tr>
<td>Type</td>
<td><b>string</b></td>
<td><b>=</b>, <b>!=</b></td>
<td>
Finds updates of a specific type, such as   "'Driver'" and "'Software'".

</td>
</tr>
<tr>
<td>DeploymentAction</td>
<td><b>string</b></td>
<td><b>=</b></td>
<td>
Finds updates that are deployed for a specific action, such as an installation or uninstallation that  the administrator of a server specifies.

"DeploymentAction='Installation'" finds updates that are deployed for installation on a destination computer. "DeploymentAction='Uninstallation'" depends on the other query criteria.

"DeploymentAction='Uninstallation'" finds updates that are deployed for uninstallation on a destination computer. "DeploymentAction='Uninstallation'" depends on the other query criteria.

If this criterion is not explicitly specified, each group of criteria that is joined to an <b>AND</b> operator implies "DeploymentAction='Installation'".

</td>
</tr>
<tr>
<td>IsAssigned</td>
<td><b>int(bool)</b></td>
<td><b>=</b></td>
<td>
Finds updates that are intended for deployment by Automatic Updates.

"IsAssigned=1" finds updates that are intended for deployment by Automatic Updates, which depends on the other query criteria. At most, one assigned Windows-based driver update is returned for each local device on a destination computer.

"IsAssigned=0" finds updates that are not intended to be  deployed by Automatic Updates.

</td>
</tr>
<tr>
<td>BrowseOnly</td>
<td><b>int(bool)</b></td>
<td><b>=</b></td>
<td>
"BrowseOnly=1" finds updates that are considered optional.

"BrowseOnly=0" finds updates that are not considered optional.

</td>
</tr>
<tr>
<td>AutoSelectOnWebSites</td>
<td><b>int(bool)</b></td>
<td><b>=</b></td>
<td>
Finds updates where the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_autoselectonwebsites">AutoSelectOnWebSites</a> property has the specified value.

"AutoSelectOnWebSites=1" finds updates that are flagged to be automatically selected by Windows Update.

"AutoSelectOnWebSites=0" finds updates that are not flagged for Automatic Updates.

</td>
</tr>
<tr>
<td>UpdateID</td>
<td><b>string(UUID)</b></td>
<td><b>=</b>, <b>!=</b></td>
<td>
Finds updates for which the value of the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateidentity-get_updateid">UpdateIdentity.UpdateID</a> property matches the specified value. Can be used with the <b>!=</b> operator to find all the updates that do not have an <b>UpdateIdentity.UpdateID</b> of the specified value.

For example, "UpdateID='12345678-9abc-def0-1234-56789abcdef0'" finds updates for <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateidentity-get_updateid">UpdateIdentity.UpdateID</a> that equal 12345678-9abc-def0-1234-56789abcdef0.

For example, "UpdateID!='12345678-9abc-def0-1234-56789abcdef0'" finds updates for  <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateidentity-get_updateid">UpdateIdentity.UpdateID</a> that are not equal to 12345678-9abc-def0-1234-56789abcdef0.



<div class="alert"><b>Note</b>  A RevisionNumber clause can be combined with an UpdateID clause that contains an <b>=</b> (equal)  operator. However, the RevisionNumber clause cannot  be combined with an UpdateID clause that contains the <b>!=</b> (not-equal) operator.</div>
<div> </div>


  
For example, "UpdateID='12345678-9abc-def0-1234-56789abcdef0' and RevisionNumber=100" can be used to find the update for <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateidentity-get_updateid">UpdateIdentity.UpdateID</a> that equals 12345678-9abc-def0-1234-56789abcdef0 and whose <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateidentity-get_revisionnumber">UpdateIdentity.RevisionNumber</a> equals 100.

</td>
</tr>
<tr>
<td>RevisionNumber</td>
<td><b>int</b></td>
<td><b>=</b></td>
<td>
Finds updates for which the value of the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateidentity-get_revisionnumber">UpdateIdentity.RevisionNumber</a> property matches the specified value.

For example, "RevisionNumber=2" finds updates where <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateidentity-get_revisionnumber">UpdateIdentity.RevisionNumber</a> equals 2.

This criterion must be combined with the UpdateID property.

</td>
</tr>
<tr>
<td>CategoryIDs</td>
<td><b>string(uuid)</b></td>
<td><b>contains</b></td>
<td>
Finds updates that belong to a specified category.

</td>
</tr>
<tr>
<td>IsInstalled</td>
<td><b>int(bool)</b></td>
<td><b>=</b></td>
<td>
Finds updates that are <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_isinstalled">installed</a> on the destination computer.

"IsInstalled=1" finds updates that are installed on the destination computer.

"IsInstalled=0" finds updates that are not installed on the destination computer.

</td>
</tr>
<tr>
<td>IsHidden</td>
<td><b>int(bool)</b></td>
<td><b>=</b></td>
<td>
Finds updates that are marked as <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_ishidden">hidden</a> on the destination computer.

"IsHidden=1" finds updates that are marked as hidden on a destination computer. When you use this clause, you can set the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates">UpdateSearcher.IncludePotentiallySupersededUpdates</a> property to <b>VARIANT_TRUE</b> so that a search returns the hidden updates. The hidden updates might be superseded by other updates in the same results.

"IsHidden=0" finds updates that are not marked as hidden. If the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates">UpdateSearcher.IncludePotentiallySupersededUpdates</a> property is set to <b>VARIANT_FALSE</b>, it is better to include that clause in the search filter string so that the updates that are superseded by hidden updates are included in the search results. <b>VARIANT_FALSE</b>  is the default value.

</td>
</tr>
<tr>
<td>IsPresent</td>
<td><b>int(bool)</b></td>
<td><b>=</b></td>
<td>
When set to 1, finds updates that are present on a computer.

"IsPresent=1" finds updates that are present on a destination  computer. If the update is valid for one or more products, the update is considered present if it is installed for one or more of the products.

"IsPresent=0" finds updates that are not installed for any product on a destination computer.

</td>
</tr>
<tr>
<td>RebootRequired</td>
<td><b>int(bool)</b></td>
<td><b>=</b></td>
<td>
Finds updates that require a computer to be restarted to complete an installation or uninstallation.

"RebootRequired=1" finds updates that require a computer to be restarted to complete an installation or uninstallation.

"RebootRequired=0" finds updates that do not require a computer to be restarted  to complete an installation or uninstallation.

</td>
</tr>
</table>
 

The default search criteria for a search are as follows:


``` syntax
( IsInstalled = 0 and IsHidden = 0 )
```

To find all the hidden updates (by using the  <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates">UpdateSearcher.IncludePotentiallySupersededUpdates</a> property set to <b>VARIANT_TRUE</b>), use the following criterion:


``` syntax
 ( IsHidden = 1 )
```


## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a>
