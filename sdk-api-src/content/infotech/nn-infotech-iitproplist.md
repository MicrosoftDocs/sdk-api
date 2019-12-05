---
UID: NN:infotech.IITPropList
title: IITPropList (infotech.h)
description: Use this interface to set properties for build objects such as word wheels and indexes. Call these methods in the document build process to define properties for all build objects.
old-location: htmlhelp\iitproplist.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitproplistinterface.htm
ms.date: 12/05/2018
ms.keywords: IITPropList, IITPropList interface [HTML Help Workshop], IITPropList interface [HTML Help Workshop],described, htmlhelp.iitproplist, infotech/IITPropList, refIITPropListInterface
ms.topic: interface
f1_keywords:
- infotech/IITPropList
dev_langs:
- c++
req.header: infotech.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Infotech.h
api_name:
- IITPropList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IITPropList interface


## -description


Use this interface to set properties for build objects such as word wheels and indexes. Call these methods in the document build process to define properties for all build objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IITPropList</b> interface inherits from <b>IPersistStreamInit</b>. <b>IITPropList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IITPropList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitproplist-clear">Clear</a>
</td>
<td align="left" width="63%">
Clears memory associated with a property list and reinitializes the list.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitproplist-get">Get</a>
</td>
<td align="left" width="63%">
Returns the property object associated with the given property ID.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitproplist-getdatasize">GetDataSize</a>
</td>
<td align="left" width="63%">
Returns the number of bytes needed to save the property data. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitproplist-getfirst">GetFirst</a>
</td>
<td align="left" width="63%">
Returns the first property object in a property list.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitproplist-getheadersize">GetHeaderSize</a>
</td>
<td align="left" width="63%">
Returns the number of bytes needed to save the header. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitproplist-savedata">SaveData</a>
</td>
<td align="left" width="63%">
Saves the data size and data from the property list to a buffer.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitproplist-saveheader">SaveHeader</a>
</td>
<td align="left" width="63%">
Saves the property ID and data type from the property list to a buffer. Only saves properties marked with a persistence state of TRUE.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitproplist-set(propid_dword_dword)">Set(PROPID,DWORD,DWORD)</a>
</td>
<td align="left" width="63%">
Sets a property to a given value or deletes a property from the list.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitproplist-set(propid_lpcwstr_dword)">Set(PROPID,LPCWSTR,DWORD)</a>
</td>
<td align="left" width="63%">
Sets a property to a given value or deletes a property from the list.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitproplist-set(propid_lpvoid_dword_dword)">Set(PROPID,LPVOID,DWORD,DWORD)</a>
</td>
<td align="left" width="63%">
Sets a property to a given value or deletes a property from the list.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitproplist-setpersist(bool)">SetPersist(BOOL)</a>
</td>
<td align="left" width="63%">
Sets the persistence state on or off for all properties.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitproplist-setpersist">SetPersist(PROPID,BOOL)</a>
</td>
<td align="left" width="63%">
Sets the persistence state on or off for a given property.



</td>
</tr>
</table> 

