---
UID: NN:wia_xp.IWiaPropertyStorage
title: IWiaPropertyStorage
author: windows-sdk-content
description: The IWiaPropertyStorage interface is used to access information about the IWiaItem object's properties. Applications must query an item to obtain its IWiaPropertyStorage interface.
old-location: wia\_wia_IWiaPropertyStorage.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiapropertystorage\iwiapropertystorage.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWiaPropertyStorage, IWiaPropertyStorage interface [WIA], IWiaPropertyStorage interface [WIA],described, _wia_IWiaPropertyStorage, wia._wia_IWiaPropertyStorage, wia_xp/IWiaPropertyStorage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wia_xp.h
req.include-header: Wia.h
req.redist: 
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
tech.root: 
req.typenames: WIAVIDEO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaPropertyStorage
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaPropertyStorage interface


## -description


The <b>IWiaPropertyStorage</b> interface is used to access information about the <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> object's properties. Applications must query an item to obtain its <b>IWiaPropertyStorage</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaPropertyStorage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWiaPropertyStorage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWiaPropertyStorage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a960b9c-d970-4feb-9282-c2b880ff3659">GetCount</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/3a960b9c-d970-4feb-9282-c2b880ff3659">IWiaPropertyStorage::GetCount</a> method returns the number of properties stored in the property storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6f2276d-7801-45a7-8e1d-35b78dfe18d5">GetPropertyAttributes</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c6f2276d-7801-45a7-8e1d-35b78dfe18d5">IWiaPropertyStorage::GetPropertyAttributes</a> method retrieves access rights and legal value information for a specified set of properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee55a613-2358-4e04-a730-64cca7b6dea2">GetPropertyStream</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ee55a613-2358-4e04-a730-64cca7b6dea2">IWiaPropertyStorage::GetPropertyStream</a> method retrieves the property stream of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44f25d8c-7f83-4c36-b582-abb6678ed78e">SetPropertyStream</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/44f25d8c-7f83-4c36-b582-abb6678ed78e">IWiaPropertyStorage::SetPropertyStream</a> sets the property stream of an item in the tree of <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> objects of a WIA hardware device.

</td>
</tr>
</table> 


## -remarks



The <b>IWiaPropertyStorage</b> interface includes several methods that are very similar to the following methods from the <a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interface. The descriptions and remarks for the IPropertyStorage version of these methods applies to the <b>IWiaPropertyStorage</b> as well. 


<table class="clsStd">
<tr>
<th>IPropertyStorage Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/a3d708fe-53af-4f1b-94ac-edc40d59a034">IPropertyStorage::ReadMultiple</a>
</td>
<td>Reads property values in a property set.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/480a2be3-ccb0-4135-a085-733f6ab48ccd">IPropertyStorage::WriteMultiple</a>
</td>
<td>Writes property values in a property set.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/95c218f1-2bf7-4946-ae9c-934e5916395a">IPropertyStorage::DeleteMultiple</a>
</td>
<td>Deletes properties in a property set.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/42b0bf7e-0402-425c-8a5f-09eaa16d93fe">IPropertyStorage::ReadPropertyNames</a>
</td>
<td>Gets string names that correspond to given property identifiers.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3612bf29-344a-4389-bd3b-56b9fa297362">IPropertyStorage::WritePropertyNames</a>
</td>
<td>Creates or changes string names that corresponds to given property identifiers.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/fedeb7fb-b84a-44a4-82d8-3a365296af69">IPropertyStorage::DeletePropertyNames</a>
</td>
<td>Deletes string names for given property identifiers.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/88c916e5-b7f0-4f4d-b049-df2b0e1c2423">IPropertyStorage::SetClass</a>
</td>
<td>Assigns a CLSID to the property set.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/00efae8b-023e-425d-b7cd-c40c17d7948e">IPropertyStorage::Commit</a>
</td>
<td>As in <a href="https://msdn.microsoft.com/72831f2c-1e07-429b-af4c-2aaced3f3888">IStorage::Commit</a>, flushes or commits changes to the property storage object.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/31e0d3e7-8575-4788-b42e-606221cf5a4c">IPropertyStorage::Revert</a>
</td>
<td>When the property storage is opened in transacted mode, discards all changes since the last commit.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/73f834cf-b6e4-4a48-bbdc-0c4ba87aacaf">IPropertyStorage::Enum</a>
</td>
<td>Creates and gets a pointer to an enumerator for properties within this set.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/46985c49-cb9b-4f67-8dff-e6fad9e188da">IPropertyStorage::Stat</a>
</td>
<td>Receives statistics about this property set.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/23c7040a-e648-4898-806d-ad01d7027cc6">IPropertyStorage::SetTimes</a>
</td>
<td>Sets modification, creation, and access times for the property set.</td>
</tr>
</table>
 



The <b>IWiaPropertyStorage</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface methods. 

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>
 

 

