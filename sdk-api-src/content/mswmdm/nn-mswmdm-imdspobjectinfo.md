---
UID: NN:mswmdm.IMDSPObjectInfo
title: IMDSPObjectInfo (mswmdm.h)
description: The IMDSPObjectInfo interface provides methods for getting and setting parameters that describe how playable objects on a storage medium are referenced or accessed by the IMDSPDeviceControl interface.
helpviewer_keywords: ["IMDSPObjectInfo","IMDSPObjectInfo interface [windows Media Device Manager]","IMDSPObjectInfo interface [windows Media Device Manager]","described","IMDSPObjectInfoInterface","mswmdm/IMDSPObjectInfo","wmdm.imdspobjectinfo"]
old-location: wmdm\imdspobjectinfo.htm
tech.root: WMDM
ms.assetid: f0003b14-7ae7-4822-befe-6bb1779328ec
ms.date: 12/05/2018
ms.keywords: IMDSPObjectInfo, IMDSPObjectInfo interface [windows Media Device Manager], IMDSPObjectInfo interface [windows Media Device Manager],described, IMDSPObjectInfoInterface, mswmdm/IMDSPObjectInfo, wmdm.imdspobjectinfo
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
 - IMDSPObjectInfo
 - mswmdm/IMDSPObjectInfo
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
 - IMDSPObjectInfo
---

# IMDSPObjectInfo interface


## -description

The <b>IMDSPObjectInfo</b> interface provides methods for getting and setting parameters that describe how playable objects on a storage medium are referenced or accessed by the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol">IMDSPDeviceControl</a> interface. Implementing this interface is optional. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

The resolution of the method parameters depends on the associated storage object as follows:

<ul>
<li>If the storage object represents a playable audio file, then the relative storage units are milliseconds.</li>
<li>If the storage object represents a folder or the root of a storage medium containing playable files, then the relative storage units are tracks.</li>
</ul>
This interface is not intended for non-playable files. If the <b>IMDSPObjectInfo</b> interface is acquired from an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage</a> interface that represents a non-playable file or a folder or a root file system containing no playable files, E_INVALIDTYPE is returned from all of the methods.

## -inheritance

The <b>IMDSPObjectInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMDSPObjectInfo</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
