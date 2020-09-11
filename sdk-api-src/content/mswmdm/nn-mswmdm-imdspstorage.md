---
UID: NN:mswmdm.IMDSPStorage
title: IMDSPStorage (mswmdm.h)
description: The IMDSPStorage interface provides an instanced-based association with a storage medium on a device.
helpviewer_keywords: ["IMDSPStorage","IMDSPStorage interface [windows Media Device Manager]","IMDSPStorage interface [windows Media Device Manager]","described","IMDSPStorageInterface","mswmdm/IMDSPStorage","wmdm.imdspstorage"]
old-location: wmdm\imdspstorage.htm
tech.root: WMDM
ms.assetid: f22b8a6d-7df8-4fea-9436-79b9ded25a40
ms.date: 12/05/2018
ms.keywords: IMDSPStorage, IMDSPStorage interface [windows Media Device Manager], IMDSPStorage interface [windows Media Device Manager],described, IMDSPStorageInterface, mswmdm/IMDSPStorage, wmdm.imdspstorage
req.header: mswmdm.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMDSPStorage
 - mswmdm/IMDSPStorage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IMDSPStorage
---

# IMDSPStorage interface


## -description

The <b>IMDSPStorage</b> interface provides an instanced-based association with a storage medium on a device. An <b>IMDSPStorage</b> interface can represent the entire storage medium, or can be further enumerated to represent any object, such as a folder or file, on that medium. This reiterative enumeration provides the mechanism for describing the organization of a hierarchically structured storage medium.

The methods of <b>IMDSPStorage</b> can be used to gather information about the object that the interface represents. The <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2">IMDSPStorage2</a> interface extends <b>IMDSPStorage</b> by getting and setting extended attributes and making it possible to get a pointer to a storage medium from its name.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPStorage</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMDSPStorage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPStorage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage">CreateStorage</a>
</td>
<td align="left" width="63%">
Creates a new storage and returns a pointer to the <b>IMDSPStorage</b> interface on the newly created storage. The new storage can be created at the same level or can be inserted into the current storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-enumstorage">EnumStorage</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of the storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes">GetAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the date on which the storage object (file or folder) was most recently modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate">GetDate</a>
</td>
<td align="left" width="63%">
Accesses the <b>IMDSPEnumStorage</b> interface to enumerate the individual storage media on a device

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getname">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the display name of the storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights">GetRights</a>
</td>
<td align="left" width="63%">
Retrieves the size of the storage object, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the <b>IMDSPStorageGlobals</b> interface to provide access to global information about a storage medium.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getstorageglobals">GetStorageGlobals</a>
</td>
<td align="left" width="63%">
Retrieves the rights information for the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-sendopaquecommand">SendOpaqueCommands</a>
</td>
<td align="left" width="63%">
Sends commands through Windows Media Device Manager. Without acting on it, Windows Media Device Manager passes the command through to a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-setattributes">SetAttributes</a>
</td>
<td align="left" width="63%">
Sets the attributes of the storage object.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage">IMDSPEnumStorage Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2">IMDSPStorage2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage3">IMDSPStorage3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4">IMDSPStorage4 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals">IMDSPStorageGlobals Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>

