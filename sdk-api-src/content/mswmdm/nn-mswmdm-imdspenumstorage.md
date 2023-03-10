---
UID: NN:mswmdm.IMDSPEnumStorage
title: IMDSPEnumStorage (mswmdm.h)
description: The IMDSPEnumStorage interface is used to enumerate the storage media on a device.
helpviewer_keywords: ["IMDSPEnumStorage","IMDSPEnumStorage interface [windows Media Device Manager]","IMDSPEnumStorage interface [windows Media Device Manager]","described","IMDSPEnumStorageInterface","mswmdm/IMDSPEnumStorage","wmdm.imdspenumstorage"]
old-location: wmdm\imdspenumstorage.htm
tech.root: WMDM
ms.assetid: fc2fed46-1f4d-4d53-a843-0f699b687a18
ms.date: 12/05/2018
ms.keywords: IMDSPEnumStorage, IMDSPEnumStorage interface [windows Media Device Manager], IMDSPEnumStorage interface [windows Media Device Manager],described, IMDSPEnumStorageInterface, mswmdm/IMDSPEnumStorage, wmdm.imdspenumstorage
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
 - IMDSPEnumStorage
 - mswmdm/IMDSPEnumStorage
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
 - IMDSPEnumStorage
---

# IMDSPEnumStorage interface


## -description

The <b>IMDSPEnumStorage</b> interface is used to enumerate the storage media on a device. For more information on the standard implementation of enumeration interfaces, see the Microsoft COM documentation, available at the Microsoft Web site. The storage media on a device are organized in a hierarchical manner similar to disk drives on a computer.

When accessed from the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-enumstorage">IMDSPDevice::EnumStorage</a> method, this interface enumerates the individual storage media on the device in the same way that you would see the individual disk drives on a computer.

When accessed from the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage">IWMDMStorage::EnumStorage</a> method, this interface enumerates the contents of the storage medium. <b>EnumStorage</b> can be called on the enumerated storage objects recursively, and thus the contents of a storage medium are returned in the hierarchical fashion in which they are stored on the storage medium. If the file system of the storage medium supports a notion of order among the content, the enumerator will return the contents in the same order.

The storage enumerator returns a snapshot of the state of storages. It may not reflect the effect of storage media insertion and removal and may not reflect the effects of subsequent <b>Insert</b>, <b>Move</b> and <b>Delete</b> methods. The client should obtain a new enumerator to get the new state of the storage media.

The <b>Insert</b>, <b>Move</b>, and <b>Delete</b> methods of the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol">IWMDMStorageControl</a> interface change the order of files. If these operations are invoked, then the order of objects as originally returned by the <b>IMDSPEnumStorage</b> interface can be changed.

If an application is going to display the order of content on a media device, the application programmer must take into account order changes that can occur as a result of <b>IWMDMStorageControl</b> operations. There are two ways to deal with this situation. One way is to simply re-enumerate whenever a change to content occurs. Another way is to maintain the order of <b>IWMDMStorage</b> objects programmatically.

No matter how this issue is handled, it must be handled by the application if the order of files is important to the application.

## -inheritance

The <b>IMDSPEnumStorage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMDSPEnumStorage</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-enumstorage">IMDSPDevice::EnumStorage</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage">IWMDMStorage::EnumStorage</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol">IWMDMStorageControl Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
