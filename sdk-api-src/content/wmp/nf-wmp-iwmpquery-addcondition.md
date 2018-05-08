---
UID: NF:wmp.IWMPQuery.addCondition
title: IWMPQuery::addCondition
author: windows-driver-content
description: The addCondition method adds a condition to the compound query using AND logic.
old-location: wmp\iwmpquery_addcondition.htm
old-project: WMP
ms.assetid: d60474ce-a785-40b1-a4fb-80dc22fddedb
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IWMPQuery interface [Windows Media Player],addCondition method, IWMPQuery.addCondition, IWMPQuery::addCondition, IWMPQueryaddCondition, addCondition, addCondition method [Windows Media Player], addCondition method [Windows Media Player],IWMPQuery interface, wmp.iwmpquery_addcondition, wmp/IWMPQuery::addCondition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPQuery.addCondition
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPQuery::addCondition


## -description



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



Conditions contained in a compound query are organized into condition groups. Multiple conditions within a condition group are always concatenated by using AND logic. Condition groups are always concatenated to each other by using OR logic. To start a new condition group, call <a href="https://msdn.microsoft.com/c81a8125-2cfa-40e2-afc5-672c2866b880">IWMPQuery::beginNextGroup</a>.

Compound queries using <b>IWMPQuery</b> are not case sensitive.

A list of values for the <i>bstrAttribute</i> parameter can be found in the <a href="https://msdn.microsoft.com/12fdeba6-14db-4689-a3cb-cb36dbc9204f">Alphabetical Attribute Reference</a> section.

The following table lists the supported values for <i>bstrOperator</i>.

<table>
<tr>
<th>
              String
            </th>
<th>
              Applies To
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




<a href="https://msdn.microsoft.com/12fdeba6-14db-4689-a3cb-cb36dbc9204f">Alphabetical Attribute Reference</a>



<a href="https://msdn.microsoft.com/b1e6bf08-3b81-4c04-92ff-73eac5f7495a">IWMPMediaCollection2::createQuery</a>



<a href="https://msdn.microsoft.com/b3d4586b-c999-447c-b974-15bd0ef160a6">IWMPMediaCollection2::getPlaylistByQuery</a>



<a href="https://msdn.microsoft.com/070bc947-bf2b-4c06-9ffa-6a23625d178a">IWMPMediaCollection2::getStringCollectionByQuery</a>



<a href="https://msdn.microsoft.com/f1f3c46f-4756-49b4-ad4f-a9097ff787f8">IWMPQuery Interface</a>
 

 

