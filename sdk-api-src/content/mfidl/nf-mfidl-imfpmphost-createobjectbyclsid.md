---
UID: NF:mfidl.IMFPMPHost.CreateObjectByCLSID
title: IMFPMPHost::CreateObjectByCLSID (mfidl.h)
description: Creates an object in the protect media path (PMP) process, from a CLSID.
helpviewer_keywords: ["787fc392-1858-41f4-a1ce-2da02a5e789f","CreateObjectByCLSID","CreateObjectByCLSID method [Media Foundation]","CreateObjectByCLSID method [Media Foundation]","IMFPMPHost interface","IMFPMPHost interface [Media Foundation]","CreateObjectByCLSID method","IMFPMPHost.CreateObjectByCLSID","IMFPMPHost::CreateObjectByCLSID","mf.imfpmphost_createobjectbyclsid","mfidl/IMFPMPHost::CreateObjectByCLSID"]
old-location: mf\imfpmphost_createobjectbyclsid.htm
tech.root: mf
ms.assetid: 787fc392-1858-41f4-a1ce-2da02a5e789f
ms.date: 12/05/2018
ms.keywords: 787fc392-1858-41f4-a1ce-2da02a5e789f, CreateObjectByCLSID, CreateObjectByCLSID method [Media Foundation], CreateObjectByCLSID method [Media Foundation],IMFPMPHost interface, IMFPMPHost interface [Media Foundation],CreateObjectByCLSID method, IMFPMPHost.CreateObjectByCLSID, IMFPMPHost::CreateObjectByCLSID, mf.imfpmphost_createobjectbyclsid, mfidl/IMFPMPHost::CreateObjectByCLSID
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFPMPHost::CreateObjectByCLSID
 - mfidl/IMFPMPHost::CreateObjectByCLSID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFPMPHost.CreateObjectByCLSID
---

# IMFPMPHost::CreateObjectByCLSID


## -description

Creates an object in the protect media path (PMP) process, from a CLSID.

## -parameters

### -param clsid [in]

The CLSID of the object to create.

### -param pStream [in]

A pointer to the <b>IStream</b> interface. This parameter can be <b>NULL</b>. If this parameter is not <b>NULL</b>, the PMP host queries the created object for the <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a> interface and calls <b>IPersistStream::Load</b>, passing in the <i>pStream</i> pointer.

### -param riid [in]

The interface identifier (IID) of the interface to retrieve.

### -param ppv [out]

Receives a pointer to the requested interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can use the <i>pStream</i> parameter to initialize the object after it is created.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphost">IMFPMPHost</a>



<a href="/windows/desktop/medfound/pmp-media-session">PMP Media Session</a>



<a href="/windows/desktop/medfound/protected-media-path">Protected Media Path</a>