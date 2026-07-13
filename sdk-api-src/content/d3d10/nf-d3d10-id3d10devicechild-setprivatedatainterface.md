---
UID: NF:d3d10.ID3D10DeviceChild.SetPrivateDataInterface
title: ID3D10DeviceChild::SetPrivateDataInterface (d3d10.h)
description: Associate an IUnknown-derived interface with this device child and associate that interface with an application-defined guid. (ID3D10DeviceChild.SetPrivateDataInterface)
helpviewer_keywords: ["ID3D10DeviceChild interface [Direct3D 10]","SetPrivateDataInterface method","ID3D10DeviceChild.SetPrivateDataInterface","ID3D10DeviceChild::SetPrivateDataInterface","SetPrivateDataInterface","SetPrivateDataInterface method [Direct3D 10]","SetPrivateDataInterface method [Direct3D 10]","ID3D10DeviceChild interface","adb67004-d0c8-2bcc-dda9-a0dbc070dbda","d3d10/ID3D10DeviceChild::SetPrivateDataInterface","direct3d10.id3d10devicechild_setprivatedatainterface"]
old-location: direct3d10\id3d10devicechild_setprivatedatainterface.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10devicechild_setprivatedatainterface.htm
ms.date: 12/05/2018
ms.keywords: ID3D10DeviceChild interface [Direct3D 10],SetPrivateDataInterface method, ID3D10DeviceChild.SetPrivateDataInterface, ID3D10DeviceChild::SetPrivateDataInterface, SetPrivateDataInterface, SetPrivateDataInterface method [Direct3D 10], SetPrivateDataInterface method [Direct3D 10],ID3D10DeviceChild interface, adb67004-d0c8-2bcc-dda9-a0dbc070dbda, d3d10/ID3D10DeviceChild::SetPrivateDataInterface, direct3d10.id3d10devicechild_setprivatedatainterface
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10DeviceChild::SetPrivateDataInterface
 - d3d10/ID3D10DeviceChild::SetPrivateDataInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10DeviceChild.SetPrivateDataInterface
---

# ID3D10DeviceChild::SetPrivateDataInterface


## -description

Associate an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>-derived interface with this device child and associate that interface with an application-defined guid.

## -parameters

### -param guid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

Guid associated with the interface.

### -param pData [in]

Type: <b>const IUnknown*</b>

A pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)-derived interface to be associated with the device child. Its reference count is incremented when set, and decremented when either the [ID3D10DeviceChild](/windows/win32/api/d3d10/nn-d3d10-id3d10devicechild) is destroyed, or when the data is overwritten by calling [SetPrivateData](/windows/win32/api/d3d10/nf-d3d10-id3d10devicechild-setprivatedata) or **SetPrivateDataInterface** with the same **GUID**.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild Interface</a>
