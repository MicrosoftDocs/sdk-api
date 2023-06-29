---
UID: NF:wmp.IWMPQuery.addCondition
title: IWMPQuery::addCondition (wmp.h)
description: The addCondition method adds a condition to the compound query using AND logic.
helpviewer_keywords: ["IWMPQuery interface [Windows Media Player]","addCondition method","IWMPQuery.addCondition","IWMPQuery::addCondition","IWMPQueryaddCondition","addCondition","addCondition method [Windows Media Player]","addCondition method [Windows Media Player]","IWMPQuery interface","wmp.iwmpquery_addcondition","wmp/IWMPQuery::addCondition"]
old-location: wmp\iwmpquery_addcondition.htm
tech.root: WMP
ms.assetid: d60474ce-a785-40b1-a4fb-80dc22fddedb
ms.date: 4/26/2023
ms.keywords: IWMPQuery interface [Windows Media Player],addCondition method, IWMPQuery.addCondition, IWMPQuery::addCondition, IWMPQueryaddCondition, addCondition, addCondition method [Windows Media Player], addCondition method [Windows Media Player],IWMPQuery interface, wmp.iwmpquery_addcondition, wmp/IWMPQuery::addCondition
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
req.target-min-winversvr: 
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPQuery::addCondition
 - wmp/IWMPQuery::addCondition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPQuery.addCondition
---

# IWMPQuery::addCondition


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>addCondition</b> method adds a condition to the compound query using AND logic.

## -parameters

### -param bstrAttribute [in]

String containing the attribute name.

### -param bstrOperator [in]

String containing the operator. See Remarks for supported values.

### -param bstrValue [in]

String containing the attribute value.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

Conditions contained in a compound query are organized into condition groups. Multiple conditions within a condition group are always concatenated by using AND logic. Condition groups are always concatenated to each other by using OR logic. To start a new condition group, call <a href="/windows/desktop/api/wmp/nf-wmp-iwmpquery-beginnextgroup">IWMPQuery::beginNextGroup</a>.

Compound queries using <b>IWMPQuery</b> are not case sensitive.

A list of values for the <i>bstrAttribute</i> parameter can be found in the <a href="/windows/desktop/WMP/alphabetical-attribute-reference">Alphabetical Attribute Reference</a> section.

The following table lists the supported values for <i>bstrOperator</i>.

<table>
<tr>
<th>String
            </th>
<th>Applies To
            </th>
</tr>
<tr>
<td>BeginsWith</td>
<td>Strings</td>
</tr>
<tr>
<td>Contains</td>
<td>Strings</td>
</tr>
<tr>
<td>Equals</td>
<td>All types</td>
</tr>
<tr>
<td>GreaterThan</td>
<td>Numbers, Dates</td>
</tr>
<tr>
<td>GreaterThanOrEquals</td>
<td>Numbers, Dates</td>
</tr>
<tr>
<td>LessThan</td>
<td>Numbers, Dates</td>
</tr>
<tr>
<td>LessThanOrEquals</td>
<td>Numbers, Dates</td>
</tr>
<tr>
<td>NotBeginsWith</td>
<td>Strings</td>
</tr>
<tr>
<td>NotContains</td>
<td>Strings</td>
</tr>
<tr>
<td>NotEquals</td>
<td>All types</td>
</tr>
</table>
 

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/WMP/alphabetical-attribute-reference">Alphabetical Attribute Reference</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-createquery">IWMPMediaCollection2::createQuery</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getplaylistbyquery">IWMPMediaCollection2::getPlaylistByQuery</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getstringcollectionbyquery">IWMPMediaCollection2::getStringCollectionByQuery</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpquery">IWMPQuery Interface</a>