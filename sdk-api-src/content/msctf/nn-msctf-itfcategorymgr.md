---
UID: NN:msctf.ITfCategoryMgr
title: ITfCategoryMgr (msctf.h)
description: The ITfCategoryMgr interface manages categories of objects for text services. The TSF manager implements this interface.helpviewer_keywords: ["ITfCategoryMgr","ITfCategoryMgr interface [Text Services Framework]","ITfCategoryMgr interface [Text Services Framework]","described","_tsf_itfcategorymgr_ref","msctf/ITfCategoryMgr","tsf.itfcategorymgr"]
old-location: tsf\itfcategorymgr.htm
tech.root: TSF
ms.assetid: 26139c8c-e1d9-4d7a-a0c0-ef73e572fbe4
ms.date: 12/05/2018
ms.keywords: ITfCategoryMgr, ITfCategoryMgr interface [Text Services Framework], ITfCategoryMgr interface [Text Services Framework],described, _tsf_itfcategorymgr_ref, msctf/ITfCategoryMgr, tsf.itfcategorymgr
f1_keywords:
- msctf/ITfCategoryMgr
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfCategoryMgr interface


## -description


The <b>ITfCategoryMgr</b> interface manages categories of objects for text services. The TSF manager implements this interface.

TSF categories help organize objects identified by a globally unique identifier ( GUID ). For example, a class identifier ( CLSID ) identifies a text service, and a GUID identifies the TSF compartment, TSF properties, and TSF display attributes. To group and organize multiple GUIDs, TSF uses category identifiers ( CATIDs).

The category manager uses an internal table, accessed with keys called GUID atoms to cache the GUIDs. Access to GUIDs is efficient using these atoms. When a GUID is obtained using its atom, the GUID description and value can be obtained from the Windows registry.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCategoryMgr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCategoryMgr</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-enumcategoriesinitem">EnumCategoriesInItem</a>
</td>
<td align="left" width="63%">
Obtains an IEnumGUID interface that enumerates all categories to which the specified GUID belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-enumitemsincategory">EnumItemsInCategory</a>
</td>
<td align="left" width="63%">
Obtains an IEnumGUID interface that enumerates all GUIDs included in the specified category.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-findclosestcategory">FindClosestCategory</a>
</td>
<td align="left" width="63%">
Finds the category closest to the specified GUID from a list of categories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-getguid">GetGUID</a>
</td>
<td align="left" width="63%">
Obtains a GUID from the internal table using its atom.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-getguiddescription">GetGUIDDescription</a>
</td>
<td align="left" width="63%">
Obtains the description of the specified GUID from the Windows registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-getguiddword">GetGUIDDWORD</a>
</td>
<td align="left" width="63%">
Obtains the DWORD value of the specified GUID from the Windows registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-isequaltfguidatom">IsEqualTfGuidAtom</a>
</td>
<td align="left" width="63%">
Determines whether the specified atom represents the specified GUID in the internal table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-registercategory">RegisterCategory</a>
</td>
<td align="left" width="63%">
Adds a specified GUID to the specified category in the Windows registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-registerguid">RegisterGUID</a>
</td>
<td align="left" width="63%">
Adds a GUID to the internal table and obtains an atom for the GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-registerguiddescription">RegisterGUIDDescription</a>
</td>
<td align="left" width="63%">
Enters a description for a GUID previously registered in the Windows registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-registerguiddword">RegisterGUIDDWORD</a>
</td>
<td align="left" width="63%">
Enters a DWORD value for a GUID previously registered in the Windows registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-unregistercategory">UnregisterCategory</a>
</td>
<td align="left" width="63%">
Removes a specified GUID from the specified category in the Windows registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-unregisterguiddescription">UnregisterGUIDDescription</a>
</td>
<td align="left" width="63%">
Removes the description for a GUID from the Windows registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-unregisterguiddword">UnregisterGUIDDWORD</a>
</td>
<td align="left" width="63%">
Removes the DWORD value for a GUID from the Windows registry.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

