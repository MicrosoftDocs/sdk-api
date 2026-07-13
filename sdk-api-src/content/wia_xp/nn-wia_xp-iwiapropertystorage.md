---
UID: NN:wia_xp.IWiaPropertyStorage
title: IWiaPropertyStorage (wia_xp.h)
description: The IWiaPropertyStorage interface is used to access information about the IWiaItem object's properties. Applications must query an item to obtain its IWiaPropertyStorage interface.
helpviewer_keywords: ["IWiaPropertyStorage","IWiaPropertyStorage interface [WIA]","IWiaPropertyStorage interface [WIA]","described","_wia_IWiaPropertyStorage","wia._wia_IWiaPropertyStorage","wia_xp/IWiaPropertyStorage"]
old-location: wia\_wia_IWiaPropertyStorage.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiapropertystorage\iwiapropertystorage.htm
ms.date: 12/05/2018
ms.keywords: IWiaPropertyStorage, IWiaPropertyStorage interface [WIA], IWiaPropertyStorage interface [WIA],described, _wia_IWiaPropertyStorage, wia._wia_IWiaPropertyStorage, wia_xp/IWiaPropertyStorage
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWiaPropertyStorage
 - wia_xp/IWiaPropertyStorage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaPropertyStorage
archived: true
---

# IWiaPropertyStorage interface


## -description

The <b>IWiaPropertyStorage</b> interface is used to access information about the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> object's properties. Applications must query an item to obtain its <b>IWiaPropertyStorage</b> interface.

## -inheritance

The <b>IWiaPropertyStorage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWiaPropertyStorage</b> also has these types of members:

## -remarks

The <b>IWiaPropertyStorage</b> interface includes several methods that are very similar to the following methods from the <a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> interface. The descriptions and remarks for the IPropertyStorage version of these methods applies to the <b>IWiaPropertyStorage</b> as well. 


<table class="clsStd">
<tr>
<th>IPropertyStorage Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-readmultiple">IPropertyStorage::ReadMultiple</a>
</td>
<td>Reads property values in a property set.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-writemultiple">IPropertyStorage::WriteMultiple</a>
</td>
<td>Writes property values in a property set.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-deletemultiple">IPropertyStorage::DeleteMultiple</a>
</td>
<td>Deletes properties in a property set.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-readpropertynames">IPropertyStorage::ReadPropertyNames</a>
</td>
<td>Gets string names that correspond to given property identifiers.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-writepropertynames">IPropertyStorage::WritePropertyNames</a>
</td>
<td>Creates or changes string names that corresponds to given property identifiers.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-deletepropertynames">IPropertyStorage::DeletePropertyNames</a>
</td>
<td>Deletes string names for given property identifiers.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-setclass">IPropertyStorage::SetClass</a>
</td>
<td>Assigns a CLSID to the property set.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-commit">IPropertyStorage::Commit</a>
</td>
<td>As in <a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a>, flushes or commits changes to the property storage object.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-revert">IPropertyStorage::Revert</a>
</td>
<td>When the property storage is opened in transacted mode, discards all changes since the last commit.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-enum">IPropertyStorage::Enum</a>
</td>
<td>Creates and gets a pointer to an enumerator for properties within this set.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-stat">IPropertyStorage::Stat</a>
</td>
<td>Receives statistics about this property set.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-settimes">IPropertyStorage::SetTimes</a>
</td>
<td>Sets modification, creation, and access times for the property set.</td>
</tr>
</table>
 



The <b>IWiaPropertyStorage</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods. 

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>
