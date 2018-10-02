---
UID: NN:msctf.ITfCategoryMgr
title: ITfCategoryMgr
author: windows-sdk-content
description: The ITfCategoryMgr interface manages categories of objects for text services. The TSF manager implements this interface.
old-location: tsf\itfcategorymgr.htm
tech.root: TSF
ms.assetid: 26139c8c-e1d9-4d7a-a0c0-ef73e572fbe4
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITfCategoryMgr, ITfCategoryMgr interface [Text Services Framework], ITfCategoryMgr interface [Text Services Framework],described, _tsf_itfcategorymgr_ref, msctf/ITfCategoryMgr, tsf.itfcategorymgr
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfCategoryMgr
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfCategoryMgr interface


## -description


The <b>ITfCategoryMgr</b> interface manages categories of objects for text services. The TSF manager implements this interface.

TSF categories help organize objects identified by a globally unique identifier ( GUID ). For example, a class identifier ( CLSID ) identifies a text service, and a GUID identifies the TSF compartment, TSF properties, and TSF display attributes. To group and organize multiple GUIDs, TSF uses category identifiers ( CATIDs).

The category manager uses an internal table, accessed with keys called GUID atoms to cache the GUIDs. Access to GUIDs is efficient using these atoms. When a GUID is obtained using its atom, the GUID description and value can be obtained from the Windows registry.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCategoryMgr</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfCategoryMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfCategoryMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/271e5fbe-54e2-47e3-97d4-cd4211b92080">EnumCategoriesInItem</a>
</td>
<td align="left" width="63%">
Obtains an IEnumGUID interface that enumerates all categories to which the specified GUID belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88b123d8-86aa-40ae-8777-1b33cfbb953a">EnumItemsInCategory</a>
</td>
<td align="left" width="63%">
Obtains an IEnumGUID interface that enumerates all GUIDs included in the specified category.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16a78457-b89c-43ef-8604-fd6c2f93f928">FindClosestCategory</a>
</td>
<td align="left" width="63%">
Finds the category closest to the specified GUID from a list of categories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5f5a67c-3152-4933-8a35-0a0cd555a0bf">GetGUID</a>
</td>
<td align="left" width="63%">
Obtains a GUID from the internal table using its atom.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0c4f64e-7e20-4dff-b597-acc280aebf32">GetGUIDDescription</a>
</td>
<td align="left" width="63%">
Obtains the description of the specified GUID from the Windows registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/016d77b5-fc08-4d2b-a9c4-50ae7926a057">GetGUIDDWORD</a>
</td>
<td align="left" width="63%">
Obtains the DWORD value of the specified GUID from the Windows registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/813916f6-610f-4031-bb17-67d7f5ffed6f">IsEqualTfGuidAtom</a>
</td>
<td align="left" width="63%">
Determines whether the specified atom represents the specified GUID in the internal table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e9a72a8-ea9b-4438-992c-5a7db64f7d82">RegisterCategory</a>
</td>
<td align="left" width="63%">
Adds a specified GUID to the specified category in the Windows registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0de17d9-be3a-4f68-a77d-880047775952">RegisterGUID</a>
</td>
<td align="left" width="63%">
Adds a GUID to the internal table and obtains an atom for the GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb42e583-af5b-42ba-9637-889c7d4bdc82">RegisterGUIDDescription</a>
</td>
<td align="left" width="63%">
Enters a description for a GUID previously registered in the Windows registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/674165f4-1624-46fa-b3c6-ee5242fa457b">RegisterGUIDDWORD</a>
</td>
<td align="left" width="63%">
Enters a DWORD value for a GUID previously registered in the Windows registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73013bc1-4623-4e00-b87b-29ea3d728e9f">UnregisterCategory</a>
</td>
<td align="left" width="63%">
Removes a specified GUID from the specified category in the Windows registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42bc1ddc-9f11-40dc-849c-2effc6efe1c8">UnregisterGUIDDescription</a>
</td>
<td align="left" width="63%">
Removes the description for a GUID from the Windows registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37161b4b-7dfc-4b8d-8e0b-3b9f794eb3b0">UnregisterGUIDDWORD</a>
</td>
<td align="left" width="63%">
Removes the DWORD value for a GUID from the Windows registry.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

