---
UID: NN:msinkaut15.IInkDivisionUnits
title: IInkDivisionUnits (msinkaut15.h)

description: Contains a collection of IInkDivisionUnit objects that are contained in an IInkDivisionResult object.
old-location: tablet\iinkdivisionunits.htm
tech.root: tablet
ms.assetid: efce8756-f42b-4d9a-bfed-4297e7e0fdec

ms.date: 12/05/2018
ms.keywords: IInkDivisionUnits, IInkDivisionUnits interface [Tablet PC], IInkDivisionUnits interface [Tablet PC],described, efce8756-f42b-4d9a-bfed-4297e7e0fdec, msinkaut15/IInkDivisionUnits, tablet.iinkdivisionunits
ms.topic: interface
f1_keywords: 
 - "msinkaut15/IInkDivisionUnits"
dev_langs:
 - c++
req.header: msinkaut15.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Inkdiv.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Inkdiv.dll
 - Inkdiv.dll.dll
api_name:
 - IInkDivisionUnits
 - IInkDivisionUnits._NewEnum
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkDivisionUnits interface


## -description



Contains a collection of <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit">IInkDivisionUnit</a> objects that are contained in an <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult">IInkDivisionResult</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDivisionUnits</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkDivisionUnits</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkDivisionUnits</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunits-item">Item</a>
</td>
<td align="left" width="63%">
Specifies the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit">IInkDivisionUnit</a> object to return at the known index in the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDivisionUnits</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>_NewEnum</b>

</td>
<td align="left" width="10%">


</td>
<td align="left" width="63%">
Gets either the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> or <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a> enumerator interface for the collection. Use this property to retrieve each object in the collection.

The <b>_NewEnum</b> property is marked restricted in the Interface Definition Language (IDL) definition for the collection interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunits-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit">IInkDivisionUnit</a> objects in the collection.

</td>
</tr>
</table> 


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype">ResultByType</a> method of the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult">IInkDivisionResult</a> object returns the requested structural elements of the analysis results in a <b>DivisionUnits</b> collection.

For more information about collections in Automation, see <a href="https://docs.microsoft.com/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult">IInkDivisionResult Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit">IInkDivisionUnit Interface</a>
 

 

