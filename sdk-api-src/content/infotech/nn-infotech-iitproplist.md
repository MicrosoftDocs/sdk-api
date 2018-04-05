---
UID: NN:infotech.IITPropList
title: IITPropList
author: windows-driver-content
description: Use this interface to set properties for build objects such as word wheels and indexes. Call these methods in the document build process to define properties for all build objects.
old-location: htmlhelp\iitproplist.htm
old-project: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitproplistinterface.htm
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IITPropList, IITPropList interface [HTML Help Workshop], IITPropList interface [HTML Help Workshop], described, htmlhelp.iitproplist, infotech/IITPropList, refIITPropListInterface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: TEXT_SOURCE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Infotech.h
api_name:
-	IITPropList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Clears memory associated with a property list and reinitializes the list.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>
</td>
<td align="left" width="63%">
Returns the property object associated with the given property ID.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83d9fa7b-d814-4293-93b9-9454c01c1503">GetDataSize</a>
</td>
<td align="left" width="63%">
Returns the number of bytes needed to save the property data. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f658126-adb4-4000-a05b-7a046bfff95d">GetFirst</a>
</td>
<td align="left" width="63%">
Returns the first property object in a property list.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73206149-cbc3-475d-8dc8-bb7547f41173">GetHeaderSize</a>
</td>
<td align="left" width="63%">
Returns the number of bytes needed to save the header. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd81bbcd-c031-4157-b213-a08bb960c6cd">SaveData</a>
</td>
<td align="left" width="63%">
Saves the data size and data from the property list to a buffer.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/576d20ed-ca23-484d-ad31-984f6d515755">SaveHeader</a>
</td>
<td align="left" width="63%">
Saves the property ID and data type from the property list to a buffer. Only saves properties marked with a persistence state of TRUE.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51dd61f7-cdd4-4cdd-808e-88900d46fb54">Set(PROPID,DWORD,DWORD)</a>
</td>
<td align="left" width="63%">
Sets a property to a given value or deletes a property from the list.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a95ff45-d918-42bd-884f-28e3fd790963">Set(PROPID,LPCWSTR,DWORD)</a>
</td>
<td align="left" width="63%">
Sets a property to a given value or deletes a property from the list.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e26cf38-eb65-4e3b-ae8f-29d35327c302">Set(PROPID,LPVOID,DWORD,DWORD)</a>
</td>
<td align="left" width="63%">
Sets a property to a given value or deletes a property from the list.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5bcb515-7567-40d5-be09-02dfe4a8c57d">SetPersist(BOOL)</a>
</td>
<td align="left" width="63%">
Sets the persistence state on or off for all properties.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12827702-2761-466b-8502-68554c477194">SetPersist(PROPID,BOOL)</a>
</td>
<td align="left" width="63%">
Sets the persistence state on or off for a given property.



</td>
</tr>
</table> 

